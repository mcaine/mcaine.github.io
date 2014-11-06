---
layout: post
title:  "Welcome to my World!"
date:   2014-11-06 14:09:40
categories: jekyll update
---
Hello and welcome. If you are reading this, you must be bored indeed.


Can I include scala code??

{% highlight scala %}
object Tables extends WithDefaultSession {

  val Tokens = new TableQuery[Tokens](new Tokens(_)) {

    def findById(tokenId: String): Option[Token] = withSession {
      implicit session =>
        val q = for {
          token <- this
          if token.uuid is tokenId
        } yield token

        q.firstOption
    }
{% endhighlight %}

