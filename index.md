---
title: /
layout: home
permalink: /
---

# Welcome

Bla bla bla bla. Bla bla bla bla bla bla bla bla.

<table>
    <th>
        <td>ID:</td>
        <td>Date: </td>
        <td>Title:</td>
    </th>
     {% for post in paginator.posts %}
        <tr>
            <td>{{ page.id }} </td>
            <td><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time> </td>
            <td><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></td>
        </tr>    
    {% endfor %}
</table>
