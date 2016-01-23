---
layout: post
title:  Getting started with RedPotion for faster iOS development
author: Andrew Havens
---

In the [previous tutorial](/blog/2016/01/19/getting-started-with-rubymotion/) we introduced you to RubyMotion for building iOS apps. RubyMotion also supports other platforms, including Android, but in this tutorial, we will continue learning about iOS development. This tutorial will introduce you to a framework called RedPotion, which will significantly improve your iOS development experience.

I like to think of RedPotion as the "Rails of iOS development". It's a collection of some of the best gems for RubyMotion, providing a toolkit of simple, intuitive APIs and DSLs for accomplishing common tasks and reducing the amount of boilerplate code you would typically write in an iOS app.

To get started using RedPotion, you need to install the gem:

{% highlight bash %}
$ gem install redpotion
Successfully installed redpotion-1.5.0
{% endhighlight %}

RedPotion comes with its own set of command line generators. Let's start by creating a new RedPotion application.

{% highlight bash %}
$ potion new redpotion_example
Creating app...
Running bundle...
Installing CocoaPods...
Installation complete!
{% endhighlight %}

Since RedPotion has a number of RubyGem and CocoaPod dependencies, the generator will automatically install these dependencies for us. Similarly to the RubyMotion generator, the RedPotion generator created an app for us to get started. Let's see what it looks like by running the app in the simulator:

{% highlight bash %}
$ cd redpotion_example
$ bundle exec rake
{% endhighlight %}

You will notice that it takes quite a bit longer to compile this app. This is because RubyMotion needs to compile every file in your app, as well as all of your dependencies. Fortunately, RubyMotion only re-compiles the files that have changed. So the next time you compile your app, it will be a lot faster.

If all goes well, you should see something that looks like this:

![RedPotion Example Screenshot](/images/redpotion_example_app.png)

If you are using the free version of RubyMotion, you probably saw an error about a missing or unsupported iOS SDK. The default RedPotion template supports iOS 7.1, but the free version of RubyMotion only supports iOS 9.2. In your `Rakefile`, change this line:

{% highlight ruby %}
app.deployment_target = '7.1'
{% endhighlight %}

...to this:

{% highlight ruby %}
app.deployment_target = '9.2'
{% endhighlight %}

## Creating Screens
TODO

## Working with Table Screens
TODO

## Working with afmotion
TODO
