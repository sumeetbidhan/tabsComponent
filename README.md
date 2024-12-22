# Tabs Component Project

This project demonstrates a simple tabs functionality built using **HTML**, **CSS**, and **JavaScript**. It allows users to switch between different content sections by clicking on tabs. The first tab is active by default, and clicking on any tab will display the corresponding content dynamically.

## Project Features
- Interactive tabs to display specific content.
- Default active tab on page load.
- Smooth transitions between tabs.
- Built using basic **HTML**, **CSS**, and **vanilla JavaScript**.


---

## How It Works
1. **HTML**: The structure consists of a container for tabs and a container for the content. Each tab is linked to a specific content section using `data-tab` attributes.
2. **CSS**: Styles are applied for an appealing layout, with classes to manage active states for tabs and content.
3. **JavaScript**: Event listeners are added to tabs. Clicking a tab updates the active states dynamically and displays the corresponding content.

---

## Technologies Used
- **HTML**: For structuring the tabs and content.
- **CSS**: For styling and transitions.
- **JavaScript**: For dynamic tab functionality using DOM manipulation and event handling.

---

## How to Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/sumeetbidhan/tabsComponent.git
   ```

2. Navigate to the project directory:
   ```bash
   cd tabsComponent
   ```

3. Open the `index.html` file in your browser:
   ```bash
   open index.html
   ```

---

## Project Code Overview
### HTML
Defines the structure for the tabs and their corresponding content.
```html
<div class="tabs-container">
  <div class="tabs">
    <button class="tab active" data-tab="tab1">Tab 1</button>
    <button class="tab" data-tab="tab2">Tab 2</button>
    <button class="tab" data-tab="tab3">Tab 3</button>
    <button class="tab" data-tab="tab4">Tab 4</button>
  </div>
  <div class="content">
    <div class="tab-content active" id="tab1">Content for Tab 1</div>
    <div class="tab-content" id="tab2">Content for Tab 2</div>
    <div class="tab-content" id="tab3">Content for Tab 3</div>
    <div class="tab-content" id="tab4">Content for Tab 4</div>
  </div>
</div>
```

### CSS
Provides styles for tabs, content, and active states.
```css
.tab.active {
  font-weight: bold;
  border-bottom: 2px solid #007bff;
}
.tab-content {
  display: none;
}
.tab-content.active {
  display: block;
}
```

### JavaScript
Handles the tab switching logic.
```javascript
document.addEventListener("DOMContentLoaded", () => {
  const tabs = document.querySelectorAll(".tab");
  const contents = document.querySelectorAll(".tab-content");

  tabs.forEach((tab) => {
    tab.addEventListener("click", () => {
      tabs.forEach((t) => t.classList.remove("active"));
      contents.forEach((c) => c.classList.remove("active"));

      tab.classList.add("active");
      const target = tab.getAttribute("data-tab");
      document.getElementById(target).classList.add("active");
    });
  });
});
```

---

## Roadmap Reference
This project is aligned with the [Simple Tabs](https://roadmap.sh/projects/simple-tabs) milestone on [Roadmap.sh](https://roadmap.sh). It is designed to enhance your understanding of:
- DOM manipulation
- Event handling
- Dynamic class management

---

## Contributing
Contributions are welcome! Please fork the repository, make changes, and submit a pull request.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Author
**Sumeet Bidhan**  
[GitHub Profile](https://github.com/sumeetbidhan)

