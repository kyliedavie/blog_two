# Blog Post #2 - Svelte Kit Project 

 > ## Introduction
<!-- Briefly desribe what we did -->
<br>

 For our third project this semester, we were tasked with creating a small-scale app using Svelte Kit that could potentially be used when selling ourselves as Junior Developers to possible employers. We wanted to differentiate ourselves from other Junior Developers by creating an app that did not feature mvp apps of last generation libraries with sloppy design and recycled code. For this project, we were responsible for creating an app that was visually pleasing, navigated to several different pages, fetched data from an API, and targeted specific data from the API of our choice. I wanted to create an app that brought in different pieces of artwork from The Art Institute of Chicago on the Gallery homepage, and then featured three different pages where artwork of a specifc characteristic was highlighted. I decided to fetch data from The Art Institute of Chicago's API using different key words describing the art as opposed to using something like an author name, media type, or date of publication. With this is mind, my app features random artwork on the first page, mountain artwork on the second page, art of sunsets on the third, and ocean artwork on the fourth page. 

<br>

 > ## Before Getting Started 
<!-- Explain what you need to know before doing this -->
<br>

Before building your app, you have to have a basic understanding of what exactly Svelte and Sveltekit are and how the terminal on your computer works and acts. [This guide to getting started with Svelte](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_getting_started) was extremely beneficial in understanding what we were going to be working with. This guide laid out what we would need to know beforehand, explained the setup of a Svelte kit, and gave a brief list and explaination of the content and commands we were going to be seing. Svelte and SvelteKit are part of the new generation of frameworks because of how they bundle the code on the developer’s end and ship only a relatively tiny amount of code. Where traditional frameworks like React and Vue do the bulk of their work in the browser, Svelte shifts that work into a compile step that happens when you build your app. It is also necessary to have a basic understanding of web development technologies such as HTML, CSS, and JavaScript and familiarity with a code editor like Visual Studio Code would also be beneficial. We used Visual Studio Code to build our apps and I found this to be realtively easy once I understood what exaclty we were doing in VS Code and where exactly I was supposed to be putting the content of my app like the HTML, CSS, and Javascript. Before getting started, it would also be extremely useful to read and follow [Part 1](https://learn.svelte.dev/tutorial/welcome-to-svelte) and [Part 2](https://learn.svelte.dev/tutorial/introducing-sveltekit) of the interactive Svelte tutorial.
<!-- 
<br>

 > ## Part of Fetch Function  
 <!-- Include code here -->

 <!-- ```bash 
# my fetch function

export async function load({ fetch }) {  
    const term = "mountain";

    const url = 'https://api.artic.edu/api/v1/artworks/search?q=' + term + '&fields=image_id,title,artist_title,date_display,medium_display,api_link' + '&limit=8';

    const artReq = await fetch(url);

    const artRes = await artReq.json();

    const artworks = artRes.data;

    return {
        artworks
    }
 ``` -->

<!-- <br> -->

<!-- ```
<script>
    export let data;
    const {artworks} = data;
    console.log(artworks);
</script>

<article>
    {#each artworks as { title, api_link, image_id, artist_title, date_display, medium_display}}
    <figure>
      <img src="https://www.artic.edu/iiif/2/{image_id}/full/843,/0/default.jpg" alt="">
      <figcaption><strong><a href="{api_link}">{title}</a></strong> by {artist_title}<br>{date_display} | {medium_display}</figcaption>
    </figure>
    {/each}
</article>

``` --> 

> ## What I learned
<!-- Explain what a **couple** parts of it do and *why* you do that -->
<br>

One of the things that I found most convenient when using Svelte was the ability to change and edit aspects of the webpage on one file as opposed to using separate HTML pages for every landing page. When you design your app with separate HTML pages, you have to go into every single HTML file and change what you want in order for it to look interchangable to the user when they navigate between pages. For example, lets say you wanted to make a change to your navigation bar. If you have four different page options for the user to select in your navigation bar, you would need to make the same change four different times if you were editing on separate HTML pages. Whereas in Svelte, you just make the change in your +layout.svelte file in your routes folder and the change occurs universally across all of your pages. Something else that I found unique to Svelte was that for this project we only needed two files for each page and we put all of our HTML, CSS and Javascript code into those two pages. Compared to how we have created our apps and websites previously where we had separate pages for our HTML, CSS and Javascript content, it was interesting to be put all three of them on one page and see how we could use the Javascript from one page to call information in the HTML of another. 

<br>

> ## Conclusion
<!-- Include a [conclusion](https://google.com) that tells us why it matters -->
<br>
At the beginning of this project, I really struggled with trying to understand *why* we were doing this and how this was any different from creating basic HTML, CSS and Javascript files in VS Code and developing an app that way. I couldn't understand why we were doing things within in the terminal and I was getting extremely frustrated because I always felt like I didn't know what the commands meant and were doing within the terminal. After I realized that I could stop using the terminal after we create our Svelte file, things started making a lot more sense to me and I was able to grasp what we were doing a lot more. I started creating new files and folders right in VS Code as opposed to using the terminal and it was much easier for me to use Svelte after I started doing that. While I didn't write my fetch functions from scratch, after looking at Professor York's repository and searching to find how he was able to call information from the public API for The Art Institute of Chicago, I was able to use his code to call my own artwork. The biggest struggle I had after calling specific artwork was trying to get the images to display within my app. It felt like everyone tried everything to get them and nothing was working but after a lot of tears and troubleshooting, we were finally able to get the images to display alongside the captions. I am very happy with the way that my app turned out because I was able to do what I set out to do: have a page displaying random artwork, then have three additional pages that displayed specific artwork of a given characteristic, and then pair all of the images with a small caption listing the title of the artwork, the artist, the date of publication, and the art medium. Overall, I feel I learned a lot about web development through this project and would likely use Svelte again after getting more familiar with the framework. 

<!-- >> Notes: keep it light and conversational. Use code blocks for code? -->

