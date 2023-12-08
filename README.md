# README

Adapted from https://www.youtube.com/watch?v=TlgSp2XPCY4

rails new blog_demo
cd blog_demo

rails g controller pages home about

rails s # start web server

rails routes # show all routes

git remote add origin https://github.com/richard-sistern/rails-blog-demo.git
  git branch -M main
  git push -u origin main

git add .
git commit -m "Add styling"
git push --set-upstream origin styling
git checkout main
git pull

git checkout -b add-blog-posts
rails g scaffold post title body:text # string is the default
rails db:migrate

rails c
Post.new # create a new post
@post = Post.new(title: "Hello world!", body: "First post!")
@post.save

- OR -
Post.create(title: "Second Post!", body: "Definitly second post!")

@post = Post.find(1) || @post = Post.first
@post.title

@post.first(2)
