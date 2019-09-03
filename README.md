# IrisPolymerV2
<h3>1) Директорию "bower_components" посемтить в корень CSP приложения</h3>
<pre>
     Пример: D:\Intersystems\TryCache2018\CSP\sys -> "csp/sys" 
             D:\Intersystems\TryCache2018\CSP\user -> "csp/user" 
</pre>


<h3>2) Импортировать классы XML:</h3>
<pre>
%ZWebNode.Lib.js.xml                      -  Библиотека js которая переопределяет встроенную cspHttpServerMethod 
%ZWebNode.PolymerV2.Components.xml        -  Контроллер сканирующий область имен, и генерирующий JS компоненты для WebComponents()
%ZWebNode.PolymerV2.ExsampleComponent.xml -  Пример компонента
%ZWebNode.PolymerV2.ExsamplePage.xml      -  Пример страницы показывающий работу Polymer
%ZWebNode.PolymerV2.Type.Array.xml        -  Тип переменной Polymer( только для коныкртирования в JS код)
%ZWebNode.PolymerV2.Type.Object.xml       -  Тип переменной Polymer( только для коныкртирования в JS код)
%ZWebNode.project.xml                     -  
%ZWebNode.Server.xml                      -  Вэб сервер
%ZWebNode.Session.xml                     -  Сессия для вэб сервера
----- Компоненты -------
%ZWebNode.PolymerV2.Element.Grid.xml      -  Элемент Grid (в разработке)
------------------------
</pre>
<h3>3) Запустить сервер</h3>
<pre>
   d ##class(%ZWebNode.Server).Start(6010,"D:\AppServ\www","index.html","UTF8")
   6010             - порт на котором будет работать вэб сервер
   "D:\AppServ\www" - Физический путь к файлам HTML которые непрописаны в вэб приложении IRIS
   "index.html"     - имя стартовой страницы если обращение идет без указания страницы
   "UTF8"           - кодировка в которую будет конвертироватся текст , который отдает сервер
</pre>
<h3>4)Запустить пример:</h3>
  <pre>
   http://localhost:6010/csp/user/%25ZWebNode.PolymerV2.ExsamplePage.cls
  </pre>