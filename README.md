# WP Bootstrap Comments

Nested Bootstrap (v3) comments for WordPress.

A comment Walker class that creates native WordPress comment lists using Bootstrap Media Object markup/classes.

See: http://getbootstrap.com/components/#media

# Installation

### From the WordPress.org plugin repository:

* Download and install using the built in WordPress plugin installer.
* Activate in the "Plugins" area of your admin by clicking the "Activate" link.
* No further setup or configuration is necessary.

### From GitHub:

* Download the [latest stable version] (https://github.com/dboutote/WP-Bootstrap-Comments/archive/master.zip).
* Extract the zip folder to your plugins directory.
* Activate in the "Plugins" area of your admin by clicking the "Activate" link.
* No further setup or configuration is necessary.


# Usage

Add a call to the `WP_Bootstrap_Comments_Walker()` class in `wp_list_comments()` in your `comments.php` template.

```
<?php
	wp_list_comments( array(
		'style'       => 'div',
		'short_ping'  => true,
		'avatar_size' => 42,
		'walker' => new WP_Bootstrap_Comments_Walker(),
	) );
?>
```

To use Bootstrap's native media list styling change `<ol class="comment-list">` to `<ul class="media-list">`.

```
<ul class="media-list">
    <?php
        wp_list_comments( array(
            'style'       => 'ul',
            'short_ping'  => true,
            'avatar_size' => 42,
            'walker' => new WP_Bootstrap_Comments_Walker(),
        ) );
    ?>
</ul><!-- .media-list -->
```