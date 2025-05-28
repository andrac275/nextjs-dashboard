## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## Chapter 1

**Commands**

Run **pnpm** i to install the project's packages.

``` 
pnpm i 
```

Followed by **pnpm dev** to start the development server.

```
pnpm dev
```

## Chapter 2

[CLSX documentation](https://github.com/lukeed/clsx)

## Chapter 3
*next/font/google* using next font, allows no additional network requests. Something that happens with custom fonts.

*next/image* module optimises images, it does the following:

- Ensure your image is responsive on different screen sizes.
- Specify image sizes for different devices.
- Prevent layout shift as the images load.
- Lazy load images that are outside the user's viewport.

*\<Image /\>* component includes those optimizations.
- Preventing layout shift automatically when images are loading.
- Resizing images to avoid shipping large images to devices with a smaller viewport.
- Lazy loading images by default (images load as they enter the viewport).
- Serving images in modern formats, like [WebP](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Image_types#webp) and [AVIF](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Image_types#avif_image), when the browser supports it.

When using Image component is important to add weight and height allowing it to know the proportions of the picture when window is resized. This will avoid *layout shift* problems due to browser having to download additional resources.

This is Image component example:
```
 <Image
        src="/hero-mobile.png"
        width={560}
        height={620}
        className="block md:hidden"
        alt="Screenshot of the dashboard project showing mobile version"
      />
```
- Notice it has width and height to avoid layout shift. 
- className is divided in 2 parts. Firts is for mobile phones and second (md) for desktop and tablets. "md" is from a certain size
    - *block md:hidden* will show the Image in phone and hide it on desktop and tablets
    - *hidden md:block* will hide on phone screens and show on desktop and tablets

## Chapter 4 Routes
- Folders inside 'app' can be used in the url (Example: *http://localhost:3000/dashboard/*) if I have a folder called "dashboard" inside "app". The folder must have a file called **page.tsx**, that's what is **public** and shown when you search for the url.
- layout.tsx file. Dashboards have some sort of navigation that is shared across multiple pages. In Next.js, you can use a special layout.tsx file to create UI that is shared between multiple pages. Check the layout.tsx file inside app/dashboard. **One benefit of using layouts in Next.js is that on navigation, only the page components update while the layout won't re-render.**



