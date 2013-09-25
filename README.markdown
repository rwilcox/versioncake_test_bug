Bug
========================

Steps to see versioncake work:

  1. bundle install
  2. rails server
  3. In browser: localhost:3000/tester
  4. You should see `HTML version of the template`.
  5. In browser: localhost:3000/tester.json
  6. You should see an error about jbuilder. This is expected (the jbuilder view is invalid)
  
Now that you've seen versioncake work you can see it fail
-------------------------

Steps to see it fail:

  1. Comment out 'jbuilder' in the Gemfile and Uncomment out 'rabl'
  2. bundle install
  3. restart rails server
  3. In browser: localhost:3000/tester
  4. You should see an error about RABL. **BUT WAIT, I WANTED HTML!!!**

An oddity
-----------------

Rename `app/views/tester/index.html.erb` to `app/views/tester/index.v1.html.erb` and see it render!
