# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

$ brew install redis

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

<!-- start the redis server. If this isn't started, you will error out! -->
$ brew services start redis 

<!-- Start the PUMA server of course...  -->
$ rails s

* Other notes
- ActionCable in it's simplest explaination is WebSockets for Rails.




<!-- go into a rails console -->
- $ rails c 
<!-- ActionCable.server.broadcast takes two parameters: "channel_name", "message" -->
<!-- this way sends basic text -->
$ ActionCable.server.broadcast "room_channel", "testing hello" 
<!-- but you can also send POJO -->
$ ActionCable.server.broadcast "room_channel", message: "hello"
