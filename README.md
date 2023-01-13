# This app uses class based component to make to do's lists.



Deploying React App on GitHub Pages
A project that just uses JavaScript, HTML and CSS is simple to host on GitHub Pages. Projects that are built in React, Vue or Angular require some configurations, though.

We will deploy the same app that we just pushed on our remote github repo.

In order for us to be able to upload our built application to GitHub Pages, we first need to install the gh-pages package.


npm i gh-pages
This package will help us to deploy our code to the gh-pages branch which will be used to host our application on GitHub Pages.

To allow us to use the gh-pages package properly, we need to add two keys to our scripts value in the package.json file:


"scripts": {
    "start": "react-scripts start",
    "predeploy": "npm run build", <----------- #1
    "deploy": "gh-pages -d build", <---------- #2
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },



Next, we need to modify our package.json file by adding the homepage field. This field is used by React to figure out the root URL in the built HTML file. In it, we will put the URL of our GitHub repository.


{
  "name": "starter-project",
  "homepage": "https://github.com/test-account-github-1/react-testing", <----
  "version": "0.1.0",
  /....
}
To deploy our application, type the following in the terminal:


npm run deploy