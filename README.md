# Company Home Page

[Codecademy WEB DEVELOPMENT FOUNDATIONS Challenge Project: Company Home Page with Flexbox](https://join.codecademy.com/learn/paths/full-stack-engineer-career-path-b/)

This is my attempt at the challenge project I'm doing for the Web Development Foundations part (Chapter 1-7) of the [Full-Stack Engineer Career Path](https://join.codecademy.com/learn/paths/full-stack-engineer-career-path-b/) I'm participating in at [Codecademy.](https://www.codecademy.com/) Check out the [live site for this project](https://andrekolmeijer.github.io/company-home-page/) to see the result.

<p>
  <img src="https://img.shields.io/github/actions/workflow/status/andrekolmeijer/company-home-page/static.yml?style=flat-square" alt="github pages build status" />
  <img src="https://img.shields.io/github/v/release/andrekolmeijer/company-home-page?style=flat-square" alt="latest semantic release" />
  <img src="https://img.shields.io/github/commit-activity/y/andrekolmeijer/company-home-page?style=flat-square" alt="commits per year" />
  <img src="https://img.shields.io/github/commit-activity/m/andrekolmeijer/company-home-page?style=flat-square" alt="commits per month" />
  <img src="https://img.shields.io/github/last-commit/andrekolmeijer/company-home-page?style=flat-square" alt="last commit" />
</p>

## What I learned

For this project I thought it would be fun to use [Copilot](https://www.bing.com/chat) for asset generation, since I had to create an imaginary company home page. I used [ChatGPT 3.5](https://chat.openai.com/chat) for concept and prompt generation. The theme I chose is Crusader Industries; a space faring company. Based on the [manufacturer](https://robertsspaceindustries.com/comm-link/spectrum-dispatch/16513-Portfolio-Crusader-Industries) from the game [Star Citizen](https://robertsspaceindustries.com/star-citizen) with the same name.

### Copilot

Turned out that Copilot is still a long way of from actually being useful. Just to name a few things:

- Can't refine upon a generated image;
- Can't upload an image for reference;
- Doesn't understand logo design;
- Can't do transparent backgrounds;
- Every image is a square;
- Can't render text accurately yet;
- Can't choose image file format; and,
- It only renders objects in close proximity.

### Scaling images

I've always been struggling with responsive imagery on the web. So when I came upon the code below I decided to experiment with it and apply it in three different ways in different sections on the web page.

```css
.container {
  width: 50%;
  height: 200px;
  overflow: hidden;
}

.container img {
  max-width: 100%;
  height: auto;
  display: block;
}
```

What I learned was:

1. An image can't take up more then a 100% of it's container and thus the only option left when wanting to crop an image is giving it a fixed with or height; and,
2. Not giving it a fixed width or height breaks the zoom functionality from the browser which might not be the best idea from an accessibility stand point.

Which leads me to believe that the best strategy for images on the web is to actually make multiple variants for web and desktop respectively. I do want to look into the `max-width` and `max-height` properties which might solve the accessibility, but I don't see how this would solve the first point as of yet.

## What's next

Since I haven't 1) optimized the site for tablets and 2) tested the site on an actual mobile device yet, there are a couple of things I still want to look into for this project:

- [ ] The `max-width` and `max-height` properties for images
- [ ] The `min-width` and `min-height` properties for images
- [ ] Text readability on mobile
- [ ] A pixel line on the right side in mobile view
- [ ] Section heights for tablets and other high dpi devices
- [ ] Menu behaviour for tablets
- [ ] The new viewport units for mobile devices (dvh/lvh/svh)

## Possibly

When looking into [variable fonts through Kevin Powell](https://youtu.be/0fVymQ7SZw0?si=G5JEfVau0BJCRoKz), I came upon a video of his that goes into [scroll-based animations](https://youtu.be/UmzFk68Bwdk?si=a0MDpXI9BmNQE6so) which I think might be fun to implement for this site.
