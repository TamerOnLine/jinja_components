# 🧩 jinja_components

**Reusable Jinja2 Components and Macros for Web Projects**

`jinja_components` is a minimal and extensible library of reusable HTML components and Jinja2 macros, designed to speed up template development in Flask, Django, and static Jinja projects.

---

## 📦 Installation

```bash
git clone https://github.com/TamerOnLine/jinja_components.git
cd jinja_components
python -m venv venv
source venv/bin/activate  # or .\venv\Scripts\Activate for Windows
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 📁 Project Structure

```
jinja_components/
├── components/           # Standalone reusable HTML blocks (cards, buttons, sections...)
├── macros/               # Modular Jinja2 macros grouped by function
├── macros.html.j2        # Central macro definitions (for inclusion)
├── style_injector.j2     # Injects dynamic style variables into templates
├── requirements.txt      # Python dependencies
├── LICENSE
└── README.md
```

---

## 💡 Usage Example

**macros.html.j2**
```jinja2
{% macro card(title, content) %}
  <div class="card">
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
  </div>
{% endmacro %}
```

**In your template:**
```jinja2
{% import 'macros.html.j2' as ui %}
{{ ui.card("Welcome", "This is a reusable card component.") }}
```

---

## 🎨 Dynamic Styling

Customize the component styles using `style_injector.j2`:

```jinja2
{% set settings = {
  "bg_color": "#f9f9f9",
  "font_family": "Tahoma",
  "border_radius": "16px"
} %}
{% include 'style_injector.j2' %}
```

---

## ✅ Goals

- ✔️ Reusability
- ✔️ Clean and semantic HTML
- ✔️ Modular structure for maintainability
- ✔️ Easy to integrate into Flask or static Jinja setups

---

## 📌 Roadmap

- [ ] Add more components (badges, alerts, navbars...)
- [ ] Add unit tests
- [ ] Add real-time theme switcher (dark/light)
- [ ] Publish on PyPI (jinja-components)

---

## 🪪 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Tamer Hamad Faour**  
[GitHub @TamerOnLine](https://github.com/TamerOnLine)