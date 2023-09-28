Команда для установки всех пакетов:
npm i gulp gulp-sass sass gulp-file-include gulp-clean gulp-server-livereload gulp-sourcemaps gulp-plumber gulp-notify gulp-group-css-media-queries --save-dev

Описание пакетов:
gulp - собственно Gulp
gulp-sass - Сборка SASS / SCSS
sass - Необходим для сборки SASS / SCSS
gulp-file-include - Подключение файлов друг в друга. HTML include
gulp-clean - Удаление файлов
gulp-server-livereload - Сервер с автообновлением страницы
gulp-sourcemaps - Исходные карты для CSS
gulp-plumber - Фикс ошибок при сборке
gulp-notify - Нотификации
gulp-group-css-media-queries - Группировка CSS медиа запросов (ломает sourcemaps), для production

Установка gulp-cli
npm install --global gulp-cli

----------------------------------------------------------------------

Сборка скриптов. webpack, babel

Установка babel:
npm i gulp-babel @babel/core @babel/preset-env --save-dev

- JS таск
- Настройки package-json
	"babel": {
  	  "presents": [
    	  "@babel/preset-env"
   	 ]
 	 }

----------------------------------------------------------------------

Установка webpack:
npm i webpack-stream style-loader css-loader --save-dev

- JS таск
- webpack конфиг:
	const config = {
 		 mode: 'production',
  	entry: {
   	 index: './src/js/index.js',
  	  // contacts: './src/js/contacts.js',
 	 },
 	 output: {
  	  filename: '[name].bundle.js',
 	 },
 	 module: {
   	 rules: [
      	{
      	  test: /\.css$/,
    	    use: ['style-loader', 'css-loader'],
  	    },
 	   ],
 	 },
	}
	module.exports = config

-----------------------------------------------------------
- пример файлов с модулями

Пример с datepicker:
npm i air-datepicker -S


JS:
import AirDatepicker from 'air-datepicker';
import 'air-datepicker/air-datepicker.css';

document.addEventListener('DOMContentLoaded', () => {
	new AirDatepicker('#my-element');
});

HTML:
<input type="text" id="my-element">

----------------------------------------------------------------------

Картинки:
npm i gulp-imagemin@7 --save-dev

.pipe(imagemin({ verbose: true }))


----------------------------------------------------------------------

Ускорение сборки

npm install gulp-changed --save-dev

- использование в картинках, HTML, JS, CSS

---------------------------------------------------------------------
Работа со стилями

объединяет импорт scss в main.scss
npm install gulp-sass-glob --save-dev


----------------------------------------------------------------------


web-p

npm i gulp-webp gulp-webp-html gulp-webp-css --save-dev


--------------------------------------------------------------------
---------------------------------------------------------------------
		для DOCS
--------------------------------------------------------------------

Автопрефикс - CSS для браузеров старых версий
npm install --save-dev gulp-autoprefixer

Сжатие стилей
npm install gulp-csso --save-dev

Сжатие html
npm install gulp-htmlclean --save-dev

Поддержка картинки webp-формата:
npm install --save-dev gulp-webp gulp-webp-html gulp-webp-css


