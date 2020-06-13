---
layout: post
title: Cleaning up a little 
---

After going through many of the basic C# courses on Pluralsight, my first personal project was to create a basic 'warm up sets' calculator. This calculator outputs reps and weights to use as warm ups before my first 'real' set (working set) of an exercise. For example, maybe I want to warm up by doing 5 reps at 50% of the weight of my first working set. If I wanted to squat 3 reps at 100kgs I would input 3 @ 100 and receive 5 @ 50 as my output. If I wanted to do multiple different warm up sets or use explicit weights instead of 'percentage of working weight' I would also be able to do that. 

When the lockdown happened I ended up putting this project aside - with most of the functionality already coded. Now, picking it up again, and before adding the final features that I would like (saving warm up set lists, and having multiple lists saved) I am going to refactor it. Having recently gone through some short courses on clean coding and defensive coding (again, on Pluralsight) I've decided that being able to cement some of those ideas in my mind by refactoring now is a good idea.

One of the first things I did, and also one of the easiest, was to identify methods and variables that needed better names. 

Clear, descriptive names help to convey design intent. In my original code I had a lot of vague, semi-useful names. I would often use "bool success = ....." for TryParse and "var input = Console.Readline();" for my use inputs. These aren't necessarily terrible but I found renaming them to be more specific definitely helps with readability - especially down the road. For exacmpt, if we later need test our success variable via "if (success) {}" will we still remember exactly what was or wasn't successful? If we used the name weightParseSuccessful instead, the intent is clear - we want to do something if the weight was parsed successfully earlier.

Related to this, I ended up renaming quite a few methods. This was not necessarily because the names needed to be more descriptive or clear but because the methods themselves needed to be refactored - leading to slightly different functionality and renaming. I'll go over some of the methods I changed in more detail in a later post but as it relates to names - if you ever feel the need to write the word 'and' in your method name, you may be asking too much of a single method. Additionally, look at your method name and then look at what your method does - the functionality it has, what it returns etc. and ask yourself if everything it does is what you'd expect given the method name. Of course sometimes it is difficuilt to say everything you want just in a name, but thinking about how you can accurately describe the intent of the method just through its name can lead to fewer headaches down the road (I'm told).

That's it for today's post. If you're reading this I hope you're having a great day.