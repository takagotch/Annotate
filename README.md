### Annotate
---

https://github.com/brentgreeff/annotate

#### Annotate_model
https://github.com/ctran/annotate_models

```ruby
# routes.rb
# id :integer(11) not null, primary key
# quantity :integer(11) not null
# product_id :integer(11)
# unit_price :float
# order_id :integer(11)
class LineItem < ActiveRecord::Base
  belongs_to :product
end

# Table name: trips
# local :geometry point, 4326
# path :geometry line_string, 4326

group :development do
  gem 'annotate'
end

group :development do
  gem 'annotate', git: 'https://github.com/ctran/annotate_models.git'
end

gem install annotate

git clone https://github.com/ctran/annotate_models.git annotate_models
cd annotate_models
rake build
gem install pkg/annotate-*.gem

cd /path/to/app
annotate

annotate --exclude fixtures
annotate --exclude tests,fixtures, factories, serializers
annotate --routes
annotate --delete
annotate --routes --delete

# -*- SkipSchmaAnnotations
rails g annotate:install

rake annotate_models
rake annotate_routes
rake remove_annotation

'skip_on_db_migrate' => 'true',

ANNOTATE_SKIP_ON_DBMIGRATE=1 rake db:migrate

--markup markdown
--markup-provider kramdown

gem 'kramdown', :groups => [:development], :require => false

git status


```


```

```





