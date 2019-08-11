# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
## Notes
Practcing Rails
Getting Started with Rails:
https://guides.rubyonrails.org/getting_started.html

Because you're working in the development environment by default, this command will apply to the database defined in the development section of your config/database.yml file. If you would like to execute migrations in another environment, for instance in production, you must explicitly pass it when invoking the command: bin/rails db:migrate RAILS_ENV=production.

STRONG PARAMS:
https://guides.rubyonrails.org/action_controller_overview.html#strong-parameters

can use:
@article = Article.new(params.require(:article).permit(:title, :text))
when reused by multiple actions can be factored out into its own private method:
private
  def article_params
    params.require(:article).permit(:title, :text)
  end

  A frequent practice is to place the standard CRUD actions in each controller in the following order: index, show, new, edit, create, update and destroy. You may use any order you choose, but keep in mind that these are public methods; as mentioned earlier in this guide, they must be placed before declaring private visibility in the controller.

  VALIDATIONS: https://guides.rubyonrails.org/active_record_validations.html

  Rails automatically wraps fields that contain an error with a div with class field_with_errors. You can define a css rule to make them standout.

  form_with documentation:
  https://api.rubyonrails.org/v5.2.3/classes/ActionView/Helpers/FormHelper.html#method-i-form_with
