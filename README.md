# PHP to HTML Form Generator
### I hate the name "Generator" - But that's what it is!

This is a simple class meant to aid you in creating forms, this is a usefull class alone when creating forms, though is mainly meant for aiding form creation on the JEK Framework http://github.com/halesyy/jek-framework, since it has some functions meant for the frontend-usage, just ignore them if you're using it with your PHP script alone!

## Simple documentation
#### It's a small class, so simple documentation!

To start, this is a simple generated form:

```php
include_once "Form.php";
$form = new Form;

$form('your_form_id')
  ->text('Username')
  ->password('Password')
  ->end();
```

Which will generate a form as you'd expect! This is the ACTUAL HTML it'd output, if that's what you want.

```html
<form id="your_form_id">
  <input type="text" placeholder="Username" name="username" />
  <input type="password" placeholder="Password" name="password" />
</form>
```

Wait... It knew I wanted to use the name **username** and **password**? How?!

Well, the way you will properly call a text input would be by ```$form->text('Username', 'username');```, but if you don't set the second paramater, it'll render as the FIRST word of the placeholder, put to LOWERCASE, so ```Some Random Placeholder``` is converted to ```some``` as the **name**, since name's are important for forms!

#More to come! Look at the class itself for more documentation.
