![ArtGallery Demo](https://github.com/shamikaredkar/ArtGallery/blob/main/ArtGalleryPreview.gif)
### Purpose:

This digital gallery features a curated selection of photos by artists like Massimo Marganoni, Giuseppe Milo, and Görlitz Photography, each presented in a sleek, responsive format that brings their work to life. Hover over images to discover the artists' names, enhancing your appreciation for the art and its creator.

---

### Features:

> Interactive overlays with artist names on hover.
> 

> Responsive design for optimal viewing on multiple devices.
> 

> Elegant and minimalistic design to highlight the photos.
> 

---

### Technology Stack:

HTML, CSS

---

### Directory Structure

```lua
/photo-blog
|-- index.html
|-- photos.css
```

---

### Code Documentation:

## HTML

</aside>

**index.html —** Contains the entire page structure.

- **`<nav>`**: This is used as the navigation or title area of the webpage.
- **`<section>`**: Each section represents a different artist's gallery.
- **`<div class="image-container">`**: This container holds each image along with an overlay for the artist's name.

```html
<section class="artist1">
  <div class="image-container">
    <img src="link_to_image" alt="Description">
    <h3>Artist Name</h3>
  </div>
  <!-- Additional image containers -->
</section>
```

##CSS
</aside>

**photos.css —** Styles the visual elements of the site.

- **`.image-container`**: Styles the containers that hold the images and the overlay text.
- **`nav`**: Styles for the navigation bar to ensure it is visually distinct.

**Image Container (`image-container`)**

```css
.image-container {
    position: relative;
    width: 30%;
    margin: calc(5%/6);
    display: inline-block;
}
```

- **Positioning**: Set to **`relative`** which allows absolute positioning of elements inside it, such as the artist's name (**`<h3>`**).
- **Display**: **`inline-block`** allows multiple containers to sit in a line horizontally, given sufficient screen width.

**Image and Hover Effects**

```css
.image-container img {
    width: 100%;
    opacity: 1;
}

.image-container:hover img{
    border-color: black;
    box-shadow: 1em 1em 1em -0.5em black;
    transform: translateY(-1em);
    opacity: 0.5;
}
```

- **Width and Opacity**: The image fills its container (**`100%`** width), and is fully opaque until hovered.
- **Hover Effects**: On hover, the image is dimmed (**`opacity: 0.5`**), lifted (**`translateY`**), and gains a shadow and border color, highlighting the image and making the text more readable.

### Artist Name (**`h3`**)

```css

.image-container h3 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: black;
    opacity: 0;
    transition: opacity 0.3s ease-in;
    width: 100%;
}
```

- **Positioning**: Positioned absolutely in the center of the **`image-container`** using percentages and the **`transform`** property. This central placement ensures the name appears over the middle of the image.
- **Visibility**: Initially hidden (**`opacity: 0`**), it becomes visible (**`opacity: 1`**) when the image container is hovered over, due to the CSS rule in **`.image-container:hover h3`**.

---

### Specific Implementations

CSS Details

- **Image Hover Effect**: The use of **`opacity`** and **`transform`** properties in the **`.image-container:hover img`** selector creates a visual effect that slightly dims the image and moves it up, making the artist's name more prominent.

Choice of Fonts

- Raleway was chosen for its modern and professional look, which complements the artistic photos.

Layout

- A grid layout allows each image to be displayed prominently, making it easy for users to engage with individual pieces of art.
