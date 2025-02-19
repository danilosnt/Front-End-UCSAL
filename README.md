## Work to Demonstrate JavaScript Practices in the Front-End Course

Demonstration of the following three functionalities using JavaScript:
- Hamburguer Menu
- Automatic SlideShow Images
- TABS

<h3>Hamburguer Menu</h3>

```js
function menuHamburguer() {
    const menu = document.getElementById("menuHamburguer");
    menu.style.width = "400px";
}
function closeMenu() {
    const menu = document.getElementById("menuHamburguer");
    menu.style.width = "0";
}
```

<h3>Automatic Slide Show</h3>

```js
document.addEventListener("DOMContentLoaded", function () {
    let slideIndex = 0;
    const slides = document.querySelectorAll(".mySlides");

    function showSlides() {
        slides.forEach(slide => slide.style.display = "none");
        slideIndex++;
        if (slideIndex > slides.length) {
            slideIndex = 1;
        }
        slides[slideIndex - 1].style.display = "block";
        setTimeout(showSlides, 3000);
    }

    showSlides();
});
```

<h3>Tabs</h3>

```js
document.addEventListener("DOMContentLoaded", function () {
    const tabButtons = document.querySelectorAll(".tabButton");
    const tabs = document.querySelectorAll(".tabs");

    tabButtons.forEach((button, index) => {
        button.addEventListener("click", function () {
            tabs.forEach(tab => tab.style.display = "none");
            tabs[index].style.display = "block";
        });
    });
});
```

Note: The website structure was provided by the professor, only the mentioned functionalities were added.
