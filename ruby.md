# ASSESSMENT 4: INTRO TO RUBY
## Interview Practice Questions

Answer the following questions. First, without external resources. Challenge yourself to answer from memory. Then, research the question to expand on your answer. Even if you feel you have answered the question completely on your own there is always something more to learn.   

1. In what ways are JavaScript and Ruby similar? In what ways are they different?

  Your answer :
    They are both object-oriented and share similar programming logic.
    JavaScript has prototypal inheritance while Ruby doesn't.
    Compare to JavaScript, Ruby's syntax reads more like natural language.

  Researched answer:

    Both JavaScript and Ruby are object-oriented, dynamic, general purpose languages and scripting languages. However, JavaScript is a front-end programming language, mainly used for client-side application, server-side and browser level interaction and changes, whereas Ruby is a back-end language by which we can generate JavaScript and HTML pages which run on server side and can interact with the database. Another difference is that Ruby is open-source so we can modify it for our needs, while JavaScript is not.

    JavaScript is also a prototype-based language while Ruby is class-based (though it is flexible enough to be programmed into having prototype-style!). Class-based languages distinguish between classes and instances (i.e. the instantiation of a class; a member of the class). Classes serve as object factories: they hold the blueprint for new objects, and can be called upon to manufacture as many as needed. Each object, or instance, has its state, but each derives its behavior from the class. Classes, in turn, share behavior through inheritance.

    A prototype-based language has the notion of a prototypical object-- an object used as a template from which to get the initial properties for a new project. Objects can specify its own properties and any object can be associated as the prototype for another object. Objects inherit directly from other objects through a prototype property, which is called Self in JavaScript.

    There are also syntactic differences such as
      1) variable declaration: longer in JS but essentially the same
      2) typeof vs class
      3) === vs ==
      4) parseInt() vs to_i
      5) incrementing: ++, += vs only +=
      6) loops: longer in JS

    In terms of performance, JavaScript is more than 20 times faster than Ruby. It is also more scalable than Ruby due to Node.JS, providing better performance with less number of servers.

    Reference:
    https://www.educba.com/javascript-vs-ruby/
    https://medium.com/learning-to-code/ruby-vs-javascript-a-quick-comparison-ebd3b63ebc49
    https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model
    https://practicingruby.com/articles/adventure-in-prototypes


2. What is a hash?

  Your answer:
    Hash is a enumerable data type composed of key and value pairs.

  Researched answer:
    In JavaScript, hashs are "hashtable" objects, which is a data structure used to implement an associative array, a structure that can map keys to values (i.e., a permutation of an associative array).

    In Ruby, hashes are like dictionaries where you can look up one thing by another thing. A hash assigns values to keys, so that values can be looked up by their keys. You can use any kind of object as keys and use any kind of object as values.

    For example, you can create key-value pairs like this:
      dictionary = { "one" => "eins", "two" => "zwei", "three" => "drei" }
      in that it is created by listing key/value pairs, separated by hash rockts, and enclosed by curly braces.
    To look up values,
      puts dictionary["one
    To set values
      dictionary["zero"] = "null"

    A hash can be nested:
      { :de => { :one => "eins", :two => "zwei", :three => "drei" } }

    Thinkgs you can do with hashes:
      1. merge 2 hashes:
        { "one" => "eins" }.merge({ "two" => "zwei" })
      2. return all the keys:
        dictionary.keys

    Reference:
    https://medium.com/@yanganif/javascript-hash-table-8878afceecbc
    http://ruby-for-beginners.rubymonstas.org/built_in_classes/hashes.html


3. What is the testing framework used in Ruby? Describe the process of setting up the testing environment.

  Your answer:
    Rspec.

  Researched answer:
    To set up a testing environment:
      1. Delete any existing test folders
      2. Add gems: add the following gems to the :development, :test group in my Gemfile and run bundle.
      3. Run Rspec Generator: rails generate rspec:install
        this will generate the app/spec/ folders
      4. Configure Rspec: open up spec/rails_helper.rb
        To use database_cleaner
          1) add require 'database_cleaner' below 'rspec/rails'
          2) change config.use_transactional_fixtures = true
          to false
          ... [other details refer to the link]
      5. Write tests

      Reference: https://medium.com/@amliving/my-rails-rspec-set-up-6451269847f9


4. Name three possible relationships between objects?

  Your answer:
   One-to-one, one-to-many, and many-to-one.

  Researched answer:
  All these relationship is based on "is a" relationship, "has-a" relationship and "part-of" relationship.

  Inheritance is an "is a " relationship. Inheritance is a parent-child relationship where we create a new class by using exsiting class.

  Association is a "has-a" type relationship, and it defines the multiplicity between objects. It can be one-to-one, one-to-many, many-to-one. If we have two classes of 'has-a' relationship, both of these entities share each other’s object for some work and at the same time they can exist without each others dependency or both have their own life time.

  Aggregation is based on "has-a" relationship and it's a special case of association and it's directional. When an object "has-a" object, then you've got an aggregation between them.

  Composition is a "part-of" relationship. Simply composition means the use of instance variables that are references to other objects. It is a special case of aggregation. When an object contains the other object, if the contained object cannot exist without the existence of container object, then it's called composition.

  Reference:
  https://www.c-sharpcorner.com/article/types-of-relationships-in-object-oriented-programming-oops/
  https://javapapers.com/oops/association-aggregation-composition-abstraction-generalization-realization-dependency/


5. What is an instance variable? How is it different from other variables in Ruby?

  Your answer:
    An instance variable is a variable with scope of a class and signified by the prefix @. It is different from other variables in that only has the scope of the class, meaning it can't be accessed outside of the class.

  Researched answer:
  Instance variables are scoped with a specific instance. This means that if you have an instance variable "title", each post will have it's own title. It has a name beginning with @ and its scope is confined to whatever object "self" refers to. From outside the object, instance variables cannot be altered or even observed, except by methods that are explicitly provided by the programmer.

  A class variable, instead, is shared across all instances of that class.

  References:
  https://stackoverflow.com/questions/7329954/instance-variable-class-variable-and-the-difference-between-them-in-ruby?rq=1
  https://ruby-doc.org/docs/ruby-doc-bundle/UsersGuide/rg/instancevars.html
  https://ruby-doc.org/docs/ruby-doc-bundle/UsersGuide/rg/instancevars.html


6. Ruby has a great community and tons of free resources to help you learn. [Here](https://www.ruby-lang.org/en/documentation/)is a list of great resources. Below are a few popular ones:
- [Interactive Ruby Tutorial](http://tryruby.org/levels/1/challenges/0)
- [Why's (poigniant) Guide to Ruby](http://poignant.guide/book/chapter-1.html): comics, anecdotes, and microscopic canaries
- [Ruby in 20 Min](https://www.ruby-lang.org/en/documentation/quickstart/)
- [Ruby Style Guide](https://rubystyle.guide/)

Choose one of these resources and look through the material for 10-15 min. List three new things you learned about Ruby:

1) Comment
#
=begin
  comment
=end

2) Convention
  1. local variables should start with a lowercase letter and words should be separated by underscores, like counter and masterful_method
  2. In Ruby, we use @ before a variable to signify that it’s an instance variable.
  3. Constants are written in all uppercase with underscores to separate words, LIKE_THIS.
  4. Ruby class and module names are also constants, but they are conventionally written using initial capital letters and camel case, LikeThis.
  5. The name of a method may end with =, !, or ?
  6. A symbol is a constant name that doesn’t require pre-declaration. Additionally, a symbol is unique 100% of the time. Symbol literals begin with “:”
  7. variables
    1) local variables starts with an underscore or lowercase letter
    2) global variable starts with $
    3) class variable starts with @@
  8. There are also reversed words

3) Bang method: Bang methods end with an exclamation mark, and often modify the object they are called on.


7. Stretch: What are blocks, procs, and lambdas?

  Your answer:

  Researched answer:
  "A closure is a first-class function with an environment. The environment is a mapping to the variables that existed when the closure was created. The closure will retain its access to these variables, even if they're defined in another scope.

  Ruby doesn't have first-class functions, but it does have closures in the form of blocks, procs and lambdas. Blocks are used for passing blocks of code to methods, and procs and lambda's allow storing blocks of code in variables."

  1. "Blocks are snippets of code that can be created to be executed later. Blocks are passed to methods that yield them within the "do" and "end" keywords."

  e.g. [1,2,3].each { |n| puts "#{n}!" }
  # a block is passed to the Array#each method, which runs the block for each item in the array and prints it to the console.

  ## Extra information to read on about the keyword "yield"

  2. A "prop" is an instance of the Proc class, which holds a code block to be executed, and can be stored in a variable. To create a proc, you call Proc.new and pass it a block.

  e.g. proc = Proc.new { |n| puts "#{n}!" }

  Tip: While it’s useful to have the proc in the method in some situations, the conversion of a block to a proc produces a performance hit. Whenever possible, use implicit blocks instead.

  3. Lambdas are special procs--they are more like regular methods in two ways: they enforce the number of arguments passed when they're called and they use normal returns. A lambda treats the return keyword the same way a method does.

  When use a lambda, it will be printed. Calling return in the lambda will behave like calling return in a method.

  Summary:
    1) Blocks are used extensively in Ruby for passing bits of code to functions. By using yield keyword, a block can be implicitly passed without having to convert it to a proc.
    2) When using parameters prefixed with ampersands (&), passing a block to a method results in a proc in the method's context. Procs behave like blocks, but they can be stored in a variable.
    3) Lambdas are procs that behave like methods, meaning return as methods instead of in their parent scope 

  References:
  https://blog.appsignal.com/2018/09/04/ruby-magic-closures-in-ruby-blocks-procs-and-lambdas.html
