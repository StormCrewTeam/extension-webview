<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
    {% for param in include.params %}
        <tr>
            <td>{{ param.name }}</td>
            <td><code>{{ param.type }}</code></td>
            <td>{{ param.desc }}

                {% if param.type == "table" %}
                {% include type-table.md fields=param.fields %}
                {% endif %}
            </td>
        </tr>
        {% endfor %}
    </tbody>
</table>