# Project 2 - *Flixster*

**Flixster** shows the latest movies currently playing in theaters. The app utilizes the Movie Database API to display images and basic information about these movies to the user and a YouTube API to play trailers.

Time spent: **13.5** hours spent in total

## User Stories

The following **required** functionality is completed:

* [x] User can **scroll through current movies** from the Movie Database API
* [x] Display a nice default [placeholder graphic](https://guides.codepath.org/android/Displaying-Images-with-the-Glide-Library#advanced-usage) for each image during loading
* [x] For each movie displayed, user can see the following details:
  * [x] Title, Poster Image, Overview (Portrait mode)
  * [x] Title, Backdrop Image, Overview (Landscape mode)
* [x] Allow user to view details of the movie including ratings and popularity within a separate activity

The following **stretch** features are implemented:

* [ ] Improved the user interface by experimenting with styling and coloring.
* [x] Apply rounded corners for the poster or background images using [Glide transformations](https://guides.codepath.org/android/Displaying-Images-with-the-Glide-Library#transformations)
* [x] Apply the popular [View Binding annotation library](http://guides.codepath.org/android/Reducing-View-Boilerplate-with-ViewBinding) to reduce boilerplate code.
* [x] Allow video trailers to be played in full-screen using the YouTubePlayerView from the details screen.


## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src=walkthrough1.gif />
<img src=walkthrough2.gif />

GIF created with [Kap](https://getkap.co/).

## Notes

I had some difficulties with the rounded corners feature for landscape mode because the image would get distorted/squished, but I managed to resize it so it takes up the full image view element. 
I also had quite a challenge with adding the video/trailer feature. I initially had difficulty understanding the way the code would work together (especially with the need to make a new Activity,
when in my mind the feature should have been a part of the details activity). Once I cleared up that, I also had difficulty grabbing the key for the video- the key was always null. This was because
the function I had that was getting the key was working asynchronously from the rest of my code where I actually tried to get that video at that key (so the key hadn't been found by the time I was
trying to find the video).

## Open-source libraries used

- [Android Async HTTP](https://github.com/loopj/android-async-http) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Android
