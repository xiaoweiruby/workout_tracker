![](https://upload-images.jianshu.io/upload_images/7680238-dc1623fa16d63ef0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```
cd newspace
git clone https://github.com/justalever/kickoff.git
cd kickoff
atom .
git fetch
rails new workout_tracker -m template.rb
What is the name of your application? Default: Kickoff workout_tracker
cd
cd newspace
cd workout_tracker
rails s
http://localhost:3000/
```
```
bundle exec rails generate apartment:install
bundle exec rails webpacker:install
yarn add webpack -cli -D
yarn add webpack-dev-server
atom .
rails g migration add_subdomain_to_users subdomain:string
rake db:migrate
rails s
```
config/initializers/apartment.rb
```
  config.tenant_names = lambda { User.pluck :subdomain }
```
app/views/devise/registrations/new.html.erb
```
    <div class="field">
      <div class="control">
        <%= f.input :subdomain, required: true, input_html: { class:"input" }, wrapper: false, label_html: { class:"label" }, hint: ("#{@minimum_password_length} characters minimum" if @minimum_password_length) %>
      </div>
    </div>
```
