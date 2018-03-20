# Q0: Why is this error being thrown?

Root routes to home#index, which attempts to access a Pokemon model that does not exist.

# Q1: How are the random Pokemon appearing? What is the common factor between all the possible Pokemon that appear? *

Seed file has pokemon without trainers.

# Question 2a: What does the following line do "<%= button_to "Throw a Pokeball!", capture_path(id: @pokemon), :class => "button medium", :method => :patch %>"? Be specific about what "capture_path(id: @pokemon)" is doing. If you're having trouble, look at the Help section in the README.


Capture_path(id: @pokemon) routes to /pokemon/id/capture, allowing us to make a button that calls the capture method for the given pokemon id, setting its trainer to the current logged in trainer.

# Question 3: What would you name your own Pokemon?

milk tea :D

# Question 4: What did you pass into the redirect_to? If it is a path, what did that path need? If it is not a path, why is it okay not to have a path here?

redirect_to trainer_path(current_trainer) 
Path needed id of current trainer in order to redirect to their profile page.  

# Question 5: Explain how putting this line "flash[:error] = @pokemon.errors.full_messages.to_sentence" shows error messages on your form.

Any errors generated while creating new pokemon are stored in @pokemon.errors.full_messages.to_sentence.  Anything put into flash is rendered on the next action, so when we display our form again after the error, our error message shows.  Using the :error key lets us use built in components for displaying errors.

# Give us feedback on the project and decal below!
Really like having the answers section since it forces us to think and not just write code/copy paste code without knowing what it is doing!  Also like how th project was broken down into sections.

# Extra credit: Link your Heroku deployed app
