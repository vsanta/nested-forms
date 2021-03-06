Nested Forms
============

jQuery plugin making it incredibly easy to implement rich behavior for your nested forms in Rails.

[Source](http://github.com/andyferra/nested-forms)


Features:
---------

- Really smart defaults
- Super flexible
- Supports nested forms inside nested forms
- Event Callbacks (after_add, after_remove)
- CSS class cycling (defaults to 'odd', 'even') (can be customized / disabled)
- Keyboard Shortcuts (SHIFT-ENTER to add) (can be disabled)
- Automatic focus on first field of added items (can be customized / disabled)
- 3.5K compressed


Simple Example
--------------

### HTML ###

    <div id="people">
      <div class="person">
        <form><!-- nested form --></form>
        <a href="#remove_person">Remove</a>
      </div>
      <a href="#add_person">Add</a>
    </div>

### Javascript ###

    $('.people').has_nested_forms('.person');


Nested, Nested Example
----------------------

### HTML ###

    <div class="people">
      <div class="person">
        <form><!-- nested form --></form>
        <a href="#remove_person">Remove</a>

        <div class="hobbies">
          <div class="hobby">
            <form><!-- nested, nested form --></form>
            <a href="#remove_hobby">Remove</a>
          </div>
          <a href="#add_hobby">Add</a>
        </div>

      </div>
      <a href="#add_person">Add</a>
    </div>

### Javascript ###

    $('.people').has_nested_forms('.person');
    $('.hobbies').has_nested_forms('.hobby', { depth: 2 });


More Customization
------------------

See the [defaults object](http://github.com/andyferra/nested-forms/blob/master/jquery-nested-forms.js#L22-34) in the plugin for a full list of options.


History
-------

### 1.0.1 ###

- Keyboard shortcuts are customizable
- Added keyboard support for deletion


### 1.0.0 ###

- Initial Release


License
-------

Copyright (c) 2010 Andy Ferra.

Dual licensed under the MIT and GPL licenses:

*  [http://www.opensource.org/licenses/mit-license.php](http://www.opensource.org/licenses/mit-license.php)
*  [http://www.gnu.org/licenses/gpl.html](http://www.gnu.org/licenses/gpl.html)
