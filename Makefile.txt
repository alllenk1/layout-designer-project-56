install:
	npm install

lint:
	npx stylelint ./src/css/*.css
	npx stylelint ./src/scss/**/*.scss
	npx htmlhint ./src/*.html

css:
	sass ./src/scss/app.scss ./src/css/app.css

watch:
	sass --watch ./src/scss/app.scss:./src/css/app.css

deploy:
	npx surge ./src/