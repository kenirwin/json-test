{% assign jsonArr = "" | split: "," %}
{% assign colors = "red,blue,green" | split: "," %}
{% for col in colors %}
{% capture jsonString %}
{ &quot;{{col}}&quot; : &quot;{{col|size}}&quot; }
{% endcapture %}
{% assign jsonArr = jsonArr | push: jsonString %}
{% endfor %}
[ {{ jsonArr | join: ","}} ]
