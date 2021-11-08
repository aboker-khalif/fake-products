What to do after cloning a laravel project:

clone the project
in the project folder:

composer install
ddev - Docker - link - https://ddev.readthedocs.io/en/stable/users/cli-usage/#laravel-quickstart

git clone https://github.com/aboker-khalif/fake-products.git
cd fake-products
ddev config --project-type=laravel
ddev composer install
ddev exec "cat .env.example | sed  -E 's/DB_(HOST|DATABASE|USERNAME|PASSWORD)=(.*)/DB_\1=db/g' > .env"
ddev exec "php artisan key:generate"
ddev launch