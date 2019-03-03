---
layout: post
title: Thoughts on using Composition vs. Inheritance
---

Today, I'll be sharing my thoughts on the use of composition versus inheritance, and when to use either approach in coding.

Firstly, let's establish what composition and inheritance are in a classic object-oriented programming language:

### Composition

The fields of a class hold a reference to another object. At the simplest level, a class uses another class to implement some of its functionality. It conveys meaning through creating wholes out of parts.

### Inheritance

A class, by default, uses the fields and methods of its superclass, where these fields and methods can be overridden to change the default behaviour. It conveys meaning by arranging concepts from generalised to specialised, and capturing the mechanics of how a class works.

----
So which is the better option for building software?
****

Most people will tell you to favour composition over inheritance. This is great as a general heuristic, but the trouble arises when it becomes a mantra. Rather than following this advice blindly, it’s important to understand the reasoning behind it. There are no silver bullets in software development, and as with anything, any tool applied inappropriately in the wrong context can easily lead to a less than satisfactory outcome. 

However, this piece of advice must have come from some place of wisdom, so we'll now look at:
* The benefits of composition
* The drawbacks to composition
* When to use inheritance

### The benefits of composition

A big benefit of using composition is that it leads to solutions that are more cohesive and less coupled. Composition-based solutions break up a problem into distinct responsibilities, and encapsulate the implementation of these into separate objects. This leads to higher cohesion, as all the separate components of the object contribute to a single well-defined task. Since all the more complex functionality is assembled by combining a series of objects that can only interact via their public interface, it encourages coding to an interface rather than an implementation, and composition-based solutions tend to rely more strongly on polymorphism than the equivalent inheritance-based implementation. As it encourages coding to an interface rather than an implementation, this also further lowers coupling and allows you to handle situations where you might want to pass in an object with a different implementation but the same interface.

Solutions with high cohesion and loose coupling are more testable and allow for quicker feedback loops. This also makes them more maintainable, and respond more easily to change, which are desirable qualities in software for a business, where what matters is the value it brings to the business at that particular point in time. A business gains a competitive edge if they can respond quickly to the changing needs of their customers over time. Therefore maintainable software that responds easily to change is in the best interest of the business, and composition-based solutions help achieve that more readily.

### The drawbacks to composition

However, some drawbacks to using composition are that it can add more indirection to a system, and it can sometimes be more work to assemble all the components together to achieve the desired behaviour.

### When to use inheritance

Sometimes the cost of the construction of a composition-based approach is higher than the benefits of encapsulated responsibilities and flexibility. Sometimes your object already has a single responsibility and you just want specialisations by augmenting your object. Or you find that using composition, you end up with one component that provides the majority of your functionality and that you’re essentially creating a wrapper for that component. Using inheritance in these cases could be a viable option.

So while inheritance certainly has its drawbacks, that isn’t to say that there is never a situation in which inheritance can be a useful approach to solving a problem. It all depends on the particular problem you’re solving.

### Conclusion

To conclude, favouring composition over inheritance as a general rule of thumb is alright. **But knowing when to use either approach leads to even better solutions.**