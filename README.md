Geckoboard Custom CSS
==========
Starter custom CSS stylesheets for styling your Geckoboard dashboards

Getting started
---
You write your own custom stylesheet based on the information presented below
or you may take one of the starter stylesheets provided here to get you started.
We provide two types of stylesheet here, one written in SCSS and a plain CSS
stylesheets more about which is explained below.

### Using plain old CSS
You may take any of the ready made CSS stylesheets from the `css` directory
and modify to your needs.

### Using SASS
We have supplied a starter CSS stylesheet written using
[Compass](http://compass-style.org/) and [SASS](http://sass-lang.com/) with
easy to configure sets of variables for changing the common elements of your

Dashboard
---
There isn't much to style on the dashboard itself. You can add a background
image or change the color using the `body` element or the `#dashboard-wrapper`
div that surrounds each dashboard. We don't advise changing fonts or colors at
this level as your custom styles may intefere with the styling of the
application when in admin mode.

Widgets
---
The anatomy of the widget in it's basic form is shown below, you can target
the individual widgets using the id which carries the unique id of each
widget shown here as `widget-{{id}}` where id is the numeric id of the widget
(`widget-12345` for example)

    <article class="widget google-analytics" id="widget-{{id}}">
      <div class="widget-inner widget-size-1x1">
        <header>
          <h1>Widget title</h1>
        </header>
        <section class="widget-body number-widget">
          <div class="widget-canvas"></div>
        </section>
        <footer></footer>
      </div>
    </article>


You can target widgets that belong to a paricular service using the service
HTML class that is assigned to each widget. The class names are the lower
case equivalent of the service title with all non-alphanumeric characters,
including spaces, replaced with a hyphen. For example Google Analytics
widgets posess the `google-analytics` HTML class name.

If you wish to alter the styling for a particluar template type across all
widgets you may target the canvas area of that widget type using the
template type HTML class name. For example all types of bullet
chart use the `bullet` template and can be targeted with `.bullet-widget` HTML
class name.

Widgets without a title posses the `no-title` HTML class on the `.widget-body`
element.
