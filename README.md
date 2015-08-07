# change-image-hover
Find the file of your theme that renders the product image on collection page. 
Look for the img tag and replace the img tag with the following code

<code>
&lt;img src="{{ product.featured_image | product_img_url: 'large' }}" {% if product.images[1] %}onmouseover="this.src='{{ product.images[1] | product_img_url: 'large' }}'" onmouseout="this.src='{{ product.images[0] | product_img_url: 'large' }}'"{% endif %} alt="{{ product.featured_image.alt | escape }}" /&gt;
</code>
