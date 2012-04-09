WordPress Sitemap with Custom Post Types
Posted on June 21, 2011 by David Kennedy
http://davidakennedy.com/blog/sitemap-with-custom-post-types/

Sitemaps offer visitors a great overview of a site�s content, and WordPress allows you to create them with ease.

Joost de Vaulk shows you how to make one version of a sitemap (http://yoast.com/html-sitemap-wordpress/). However, it doesn�t include an option for custom post types, which have become more popular since WordPress 3.0 came out.

Here�s how to make that happen, building on Joost�s example.
The Code

You�ll want to start out with Joost�s code because it works perfectly, and will give you just what you need for your posts and pages.

You�ll see a few things happening here:

* We�re setting up a basic unordered list, based on our custom taxonomy and listing posts in our custom post type by title.
* In the second chunk of code, we�re using a new WP Query to query the posts for our custom post type and custom taxonomy.

You�ll need to change the code in a few key places.

$terms = get_terms( 'my_taxonomy', 'orderby=name' );

Change the above code the your custom taxonomy name.

'post_type' => 'my_posttype',

Change the above code the your custom post type name.

'taxonomy' => 'my_taxonomy',

Change the above code the your custom taxonomy name.

Wrapping It Up
That does it. Now, whenever you add posts to your post type and taxonomy, it gets automatically added to the sitemap.

Nice!

You can see an example on my own sitemap. Huge thanks to Joost for a great code snippet! And thanks to Joeleen Kennedy (http://joeleen.net) for helping me figure this one out.