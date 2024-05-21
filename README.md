# NHS Screening design library

A central space for UCD teams in Screening to share their work and ideas. 

## Running the application locally

### Prerequisite

Install the long-term support (LTS) version of <a href="https://nodejs.org/en/">Node.js</a>, which includes npm.

### Cloning and running the application

Clone the repo: `git clone https://github.com/nhsuk/screening-library.git screening-library` and while in the project directory `cd screening-library`, install the required npm packages with: `npm install`.

Run the project in development mode `npm run watch` and visit <a href="http://localhost:3000">http://localhost:3000</a>.

Run automated tests locally with `npm run test`.

## Adding designs to the library

Decide whether the design you're adding is a style, component or pattern and open the relevant folder in `views/design-library`.

Duplicate the `template` folder and rename it to the name of your style, component or pattern.

There are 3 documents in `template/default`. These are the HTML, CSS and JS files where you will add the code for your design.

In your newly created folder, update the files inside `default` as follows:

    1. Add your design's HTML code to `index.njk`
    2. Add your design's CSS or SASS to `styles.scss`
    3. If your design requires JavaScript, add your code to `scripts.js`. This is not mandatory if your design does not require JavaScript

You can repeat these steps if you have more than 1 variation of your design. Either duplicate the `default` folder you just updated, or the `variant` folder inside `template` as many times as you require. Make sure to give each new folder a unique, indentifiable name as we will reference them later when building our index page.

The basic page structure is defined in `template/index.njk`. Update this file in your new folder with the details of your design, including the rationale, where the design was used, the associated research and the contact details for your team.

Using the `designExample` macro on line 21 of `template/index.njk`, add the designs from your `default` folder by referencing them in the following way:

    1. On line 22, set `group` to `styles`, `components` or `patterns` depending on the type of design you've added.
    2. On line 23, set `item` to the name of the design you are adding. 
    3. On line 24, set `type` to `default`, or the name of the folder you are referencing if you have created a variation of your design.

When you have finished adding your designs, update the relevant section at lines 7-17 of `views/includes/_side-nav.njk` to include the name and URL of your newly added design.

You may also wish to update the 'What's new' section at line 27 of `views/index.njk`.

## Get in touch

The NHS Screening design library is maintained by the Digital Transformation of Screening team. [Email Dan Johnston](mailto:daniel.johnston1@nhs.net) if you have any questions about it's use.

## Licence

The codebase is released under the MIT Licence, unless stated otherwise. This covers both the codebase and any sample code in the documentation. The documentation is © Crown copyright and available under the terms of the Open Government 3.0 licence.
