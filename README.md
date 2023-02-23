
<br />
<div align="center">
  <h3 align="center">Read Me File</h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>Folder Structure With Descriptions
        <li><a href="folder-structure-with-descriptions">Folder Structure With Descriptions</a></li>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#running-the-tests-on-local">Running the tests On Local</a></li>
        <li><a href="#running-the-tests-in-the-pipeline-with-github-actions">Running the tests in the pipeline with Github actions</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Api automation for some functionalities including :
* Authentication
* Wallet
* Transfer



<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

The automation project was done with Postman and can be run on both the postman application and Newman which is what will be explained in this ReadMe
The tests are also integrated into github actions, so the tests can run in a pipeline here

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

### Folder Structure With Descriptions

|                   |               |                                                                                          |
| ----------------- | ------------- | ---------------------------------------------------------------------------------------- |
| QA Engineer Assessment Copy.json  | Contains all the tests                                                                   |
|                   | jsconfig.json | Eslint settings                                                                          |
| /.github.         | /workflows    | Github actions configurations                                                            |


To get a local copy up and running follow these simple example steps.

### Prerequisites

* npm
  ```sh
  npm install npm@latest -g
  ```
* Newman
  ```sh
  npm install -g newman-reporter-html
  ```
* Download postman/postman web

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/tobi-legan/ui-automation-assignment.git
   ```
2. Import the file on postman desktop/web

### Running the tests On Local

Two ways of running this

#### Postman web/Desktop

1. Open the collection on postman and click on the collection
2. Right click on the collection and select Run Collection
3. Click on run flow, it will run all the flows


#### Newman CLI
1. Open terminal on the root folder of the cloned repo and run 
   ```sh
   newman run "QA Engineer Assessment Copy.postman_collection.json"
   ```
2. It should run the tests


### Running the tests in the pipeline with Github actions

#### A bit of background on the github actions configuration.
to see the file, go to ./github/workflows/newman.yml
![Screenshot 2023-02-23 at 4 04 45 AM](https://user-images.githubusercontent.com/69557328/220813697-6797b30d-0392-4f0c-a6d2-f9d72feb334a.png)

1. It is triggered on push automatically in this repo so you can also push some code to this repo and it will trigger the actions as seen in the screen shot below for one of the PRs

2. For generating the html report, you will see an artifact called RunReports that you can download to see the results in case of test failures

#### To run it now without pushing any code to the repo

1. Click the Actions menu bar in github for the repo
![Screenshot 2023-02-23 at 4 01 59 AM](https://user-images.githubusercontent.com/69557328/220813941-4786398d-615f-4b96-a80f-acebca1cd6dd.png)


2. Click on the latest run for the 'Main' branch

3. Click on the re-run button on the page
![Screenshot 2023-02-23 at 4 03 41 AM](https://user-images.githubusercontent.com/69557328/220813963-0cc35123-017e-48f0-bb16-e0955deb3904.png)


4. It should start running and you should see the results in the pipeline as well as the generated RunReport artifact



<p align="right">(<a href="#readme-top">back to top</a>)</p>
