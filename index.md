
<p style="text-align:center;">Here are a collection of city guides to help you find the most convenient location and best deal when storing your luggage</p>

<div class="row text-center p-4">
    {% for category in site.categories %}
    <h2 class="text-left pt-5 pb-5">{{ category | first | strip_html }}</h2>
        {% for post in category.last %}
            <div class="col-12 col-md-4 p-3">
                <a class="w-100 text-dark" style="text-decoration: none" href="{{ post.url }}">
                    <img class="img-thumbnail rounded" src="/thumbnail/{{post.categories[0] | slugify }}/{{ post.city | slugify }}.jpeg" />
                    <h3 class="pt-2">{{ post.city }}</h3>
                </a>
            </div>
        {% endfor %}
    {% endfor %}
</div>