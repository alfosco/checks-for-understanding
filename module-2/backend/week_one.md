## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

        Post - submits data to a specified resource
        Get - retrieves data from a specified resource
        Put - updates a resource completely through a specified resource
        Delete - deletes a specified resource
        I believe the fifth verb is 'Patch' and it does the same thing as 'Put'.
        
2. What is Sinatra?

        A DSL that enables you to easily create web applications in Ruby.
        
4. What is MVC?

        It's an acronym for Model, View, Controller. This is a software design pattern for implementing user interfaces on computers.
        
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

        It simplfifies desicion making when creating an application. There is no need to waste time on how you will name your paths because that convention is already implemented in Sinatra. You can of course deviate from this convention but it will require you to write more code.

6. What types of variables are accessible in our view templates without explicitly passing them?

        All of the corresponding model's attributes and methods.

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
  @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses/:name' do
    erb :index, :locals => {:name => params[:name]}
  end
  ```

9. What's the purpose of ERB?

        It allows you to embedd Ruby into a text or HTML document.

10. Why do I need a development AND test database?

        There are two databases so tests that are run do not corrupt the data in your development database.

11. What's responsive design?

        It's an approach to web design aimed at allowing desktop webpages to be viewed in response to the size of the screen or web browser someone is viewing with. 

12. What is CRUD and why is it important?

        It's an acronym for CREATE, READ, UPDATE, and DELETE. These are the major functions that are implemented in relational database applications.

13. What does HTTP stand for?

        Hypertext Transfer Protocal.

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

        <% %> Runs the Ruby inside of it but doesn't display it
        <%= %> Displays the Ruby that is being run inside of it

15. What's an ORM?

        Object Relational Mapping. It connects the rich objects of an application to tables in a relational database management system. The properties and relationships of the objects in an application can be easily stored and retrieved from a database without writing SQL statements directly

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

        Active Record

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

get '/restaurants'

        Displays a list of all restaurants.

get '/restaurants/new'

        Return an HTML form for creating a new restaurant.

post '/restaurants'

        Create a new restaurant.

get '/restaurants/:id/edit'

        Return an HTML form for editing a restaurant.

put '/restaurants/:id'

        Update a specific restaurant.

get '/restaurants/:id'

        Display a specific restaurant.

delete '/restaurants/:id'

        Delete a specific restaurant.

18. What's a migration?

        A migration alters your database schema over time. Each migration modifies your schema to add or remove tables, columns, or entries.

19. When you create a migration, does it automatically modify your database?

        I believe it only modifies your database if you format your migration table for new changes.

20. How does a model relate to a database?

        A model is mapped to its corresponding table in the database. This enables you to have the ability to map the columns of each row in that table with the attributes of the instances of your model.

21. What's the difference between agile workflow and waterfall method?

        The Agile workflow involves working on small modules, and responding to users' changed requirements rather than following a specific or predetermined plan of action. The Waterfall method is a sequential design process where the completion of one stage leads to another.

22. What is the difference between `#new` and `#create`?

        'New' will create a new instance but will not save it to the database. 'Create' will create a new instance and save it to the database.
