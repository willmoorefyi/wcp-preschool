WCP Preschool website
=====================

## Building

This website is written in markdown and built with [jekyll](https://jekyllrb.com/).  Jekyll is a mature and
well-documented static site generator.  Refer to the documentation for instructions on how to setup / run.

## Publishing

Make sure that you have compiled the website for distribution prior to publishing to S3.  To do this, run the `build`
jekyll command:

`bundle exec jekyll build`

This app uses the [s3 gem](https://github.com/laurilehmijoki/s3_website) to push compiled assets to S3 and manage
cloudfront invalidation.  To execute, follow the instructions to install the gem and execute via:

```
s3_website push
```

make sure that proper credentials for the s3 bucket are stored in your `~/.aws/credentials.` file
