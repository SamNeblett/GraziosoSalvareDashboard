# CS 340 Project Two README - Grazioso Salvare Dashboard

## About the Project: Grazioso Salvare Animal Database Management

This project is built by Global Rain for use in aiding in the operations
of international rescue-animal training company Grazioso Salvare. This
project utilizes a CRUD (Create, Read, Update, and Delete) module,
previously built by Global Rain, which accesses Grazioso Salvare’s
animal shelter database (MongoDB). This project is an interactive,
web-based dashboard for Grazioso Salvare to aid in identifying and
categorizing available dogs from their animal shelters. This dashboard
gives Grazioso Salvare the ability to visualize dog and shelter data in
an interactive web application, capable of various levels of
interactivity including the ability to sort on multiple fields, filter
for rescue purposes, and display known locations.

This project follows the Model-View-Controller (MVC) model pattern,
consisting of a base level database model using NoSQL and MongoDB, a
dashboard client level built with Python and the Dash framework, and a
Python-based “glue” level acting as the controller between levels. Users
with sufficient database access can create new entries in the Grazioso
Salvare animal database, as well as read existing entries, update
existing entries, and delete existing entries, but functionality from
the client-level dashboard is limited to Read queries, due to the
client’s goal of identifying and categorizing available dogs for various
needs from the dashboard view.

## Motivation

The motivation for this project is to address the need Grazioso Salvare
has in managing their database of animals. MongoDB was chosen to handle
the databases and documents due to its robust scaling capabilities and
flexible requirements. Python was chosen due to its compatibility and
ubiquity in the database management space for middle-ware modules and
frontends.

**Required Functionality**

The client, Grazioso Salvare, stated they are looking for a dashboard
that has the following functions:

- Displays company branding via logo image

- Displays a unique identifier from the developer

- Interactive options to filter the Austin Animal Center Outcomes data
  set

- A data table that dynamically responds to the filtering options and
  displays matches

- A geolocation map and a second chart of your choice that dynamically
  respond to the filtering options

- A pie chart to display dog breed distributions based on the filtered
  data

- The ability to connect to the backed shelter database (MongoDB)

- Demonstrating the execution of the “Water Rescue” filtering option on
  the dashboard:

<img width="1082" height="550" alt="image" src="https://github.com/user-attachments/assets/bdc733ea-dcca-48af-aff3-39b08c90602e" />

- Demonstrating the execution of the “Mountain or Wilderness Rescue”
  filtering option on the dashboard:

<img width="1077" height="548" alt="image" src="https://github.com/user-attachments/assets/0e4849db-a1e2-407e-9359-464a8144f507" />

- Demonstrating the execution of the “Disaster or Individual Tracking”
  filtering option on the dashboard:

<img width="1091" height="554" alt="image" src="https://github.com/user-attachments/assets/7d40c466-d9e2-4401-8d7c-fb45bed9185b" />

- Demonstrating the execution of the “Reset” filtering option on the
  dashboard, which returns all widgets to their original, unfiltered
  state:

<img width="1094" height="556" alt="image" src="https://github.com/user-attachments/assets/b2e26cf5-e9e6-47fc-8f8f-fa0a7b079b41" />

## Tools Used to Achieve Dashboard Functionality

- Terminal with Bash

  - Terminal required for using Bash, and as an interface to navigate
    through datasets.

  - Bash required for using configuring and manipulating datasets with
    MongoDB.

  - Resources:

    - <https://linuxcommand.org/lc3_man_page_index.php>

    - <https://www.mongodb.com/docs/database-tools/mongoimport/>

- MongoDB

  - Chosen as the base-level model component of the development of the
    Grazioso Salvare Dashboard due its ability to function as a NoSQL
    database, useful for this project as the data sources so far are in
    the Comma-Separated Value (CSV) format and ease of use in
    manipulating datasets with JavaScript Object Notation (JSON) strings
    from CRUD (Create, Read, Update, and Delete) middle-ware
    applications.

  - Required for NoSQL database functionality, used for creating,
    reading, updating, and deleting records in the Grazioso Salvare
    Animal Database.

  - Resources:

    - Textbook “Mastering MongoDB 6.x : Expert Techniques to Run
      High-volume and Fault-tolerant Database Solutions Using MongoDB
      6.x”

      - <https://research.ebsco.com/c/cyb354/ebook-viewer/epub/6rs46l7ncj>

    - <https://www.mongodb.com/docs/database-tools/mongoimport/>

- Python 3

  - Chosen as the programming language used to develop and update the
    database CRUD module (“CRUD_Python_Module.py”) and Jupyter Notebook
    files (all .ipynb files), as well as its interoperability with
    backend services, such as MongoDB through PyMongo, middle-ware
    capability, and client-level web-app functionality with Dash.

  - Resources:

    - Textbook “Head First Python, 2nd Edition”

      - <https://learning.oreilly.com/library/view/head-first-python/9781491919521/>

    - <https://www.mongodb.com/docs/languages/python/pymongo-driver/current/>

- Dash Framework

  - Chosen as the framework to build the client-facing, interactive web
    dashboard due its ability to easily create web interfaces with
    Python.

  - Provides the client-facing view of the MVC model pattern via the web
    dashboard, as well as the interactivity and control on the dashboard
    to manipulate data tables, filters, and graphs.

  - Resources:

    - <https://dash.plotly.com/dash-core-components>

    - <https://dash.plotly.com/datatable>

    - <https://dash-leaflet-docs.onrender.com/>

- Plotly Express

  - Graphing library used to display data as a pie chart on the
    dashboard, chosen due to its compatibility with Python and Dash.

  - Resources:

    - <https://plotly.com/python/pie-charts/>

- Codio (Optional, but recommended)

  - Development environment used for the development of this project.
    Provides access to Terminal, Bash, MongoDB, Python 3, Jupyter Lab,
    Jupyter Notebook, and cloud storage for project files and the
    project database. Codio is highly recommended for this project.

  - Resources:

    - <https://codio.com/>

    - <https://learn.snhu.edu/content/enforced/2019719-CS-340-10397.202581-1/course_documents/CS%20340%20Mongo%20in%20Codio%20(Virtual%20Lab)%20Tutorial.pdf>

- Jupyter Lab and Jupyter Notebook

  - Web-based IDE utilized for writing, storing, and using the CRUD
    module (“CRUD_Python_Module.py”), all Jupyter Notebook files
    (.ipynb), chosen for its compatibility with Python, Jupyter Notebook
    files, and ease of deployment.

  - Jupyter Notebook is a component of Jupyter Lab, required for running
    all Jupyter Notebook files (.ipynb), including the Grazioso Salvare
    Dashboard and CRUD module tests.

  - Resources:

    - <https://learn.snhu.edu/content/enforced/2019719-CS-340-10397.202581-1/course_documents/CS%20340%20Using%20Jupyter%20Labs%20in%20Codio%20(Virtual%20Lab)%20Tutorial.pdf>

**Steps Taken to Complete the Project**

1.  The database was originally set up for the client in Project One,
    where the Austin Animal Center Outcomes dataset was imported into
    the aac MongoDB database using mongoimport from the terminal, along
    with the aacuser to access the database.

2.  The CRUD Python module was developed as the AnimalShelter class with
    the goal of enabling CRUD (Create, Read, Update, and Delete)
    functionality on the database.

3.  Testing cases were then written as part of Project One, which test
    Create, Read, Update, and Delete functionality on the database
    through the CRUD Python module.

4.  Initial dashboard components were then developed using Jupyter
    Notebook files and the Dash framework in Module 6. Components
    included an interactive data table to display shelter data and an
    interactive map to display locations of animals in the shelter data.
    This functionality was later brought into the final dashboard code,
    ProjectTwoDashboard.ipynb.

5.  Interactive filtering was then developed as radio items for the
    dashboard, which when selected, filtered the data table dynamically
    through the update_dashboard method on ProjectTwoDashboard.ipynb,
    which called the read method on the CRUD Python module
    (CRUD_Python_Module.py).

6.  A pie chart was then developed to match the concept images given by
    the client, which functions via the update_graphs on
    ProjectTwoDashboard.ipynb to display dog breed distributions based
    on the filtered data.

7.  Final testing of the dashboard and documentation for the client was
    then performed, including the writing of this README document.

## Getting Started with the Dashboard

To get a local copy of the dashboard up and running, follow these simple
example steps:

1.  Enroll in CS 340 at SNHU

<img width="183" height="221" alt="image" src="https://github.com/user-attachments/assets/f856e575-8962-4fc2-b13e-c18107f869db" />

2.  Open Codio, enter the Jupyter Lab tab, and open the
    “ProjectTwoDashboard.ipynb” file.

<img width="644" height="382" alt="image" src="https://github.com/user-attachments/assets/71d12597-acd8-4f56-a85c-bdf7f6f83d65" />

<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/417cd11f-3479-4aeb-acaa-111f7c7fbaeb" />

3.  Scroll down on the “ProjectTwoDashboard.ipynb” document, press the
    Play button at the top of the code view, then select click on the
    URL given by the Jupyter Notebook file displaying where the Dash app
    (the Grazioso Salvare Dashboard) is running.

<img width="975" height="480" alt="image" src="https://github.com/user-attachments/assets/46988fa5-6fdf-475c-9460-be75303769c9" />

4.  Observe the completed Dashboard, optionally interact with various
    elements on the dashboard to view how the data table and graphs
    react.

<img width="975" height="497" alt="image" src="https://github.com/user-attachments/assets/a2b5bb34-d71b-4f8c-a51c-fb5f08ae7567" />

## Getting Started with the CRUD Module

To get a local copy of the CRUD module up and running, follow these
simple example steps:

1.  Enroll in CS 340 at SNHU

<img width="183" height="221" alt="image" src="https://github.com/user-attachments/assets/dd7773d5-6147-42a9-b06b-1919c3d643b7" />

2.  Open Codio and enter the Terminal tab, if it is not opened by
    default.

<img width="644" height="382" alt="image" src="https://github.com/user-attachments/assets/1ee01c0e-c364-4337-bef3-6425f9b4394e" />

<img width="975" height="91" alt="image" src="https://github.com/user-attachments/assets/8f5bacc3-edec-4a0e-a1c7-245b214cbe4e" />

3.  If the Animal Shelter dataset is not already imported in your local
    copy, run the following commands in a Codio terminal to import the
    dataset into a MongoDB instance:

    1.  mongoimport --db aac --collection animals --drop --type csv
        --headerline --file ./aac_shelter_outcomes.csv

<img width="975" height="103" alt="image" src="https://github.com/user-attachments/assets/fa27b44a-3eac-4661-9f38-ecbde9ad0cfe" />

4.  If an aacuser account has not yet been set up on your local copy,
    run the following commands in a Codio terminal to set up and create
    the applicable user in the aac database, and enter a password for
    the new “aacuser” account when prompted:

    1.  cd ./datasets

    2.  mongoimport --type=csv --headerline --db aac --collection
        animals --drop ./aac_shelter_outcomes.csv

    3.  mongosh

    4.  use admin

    5.  db.createUser( { user: "aacuser", pwd: passwordPrompt(), roles:
        \[ { role: "readWrite", db: "aac" } \] } )

<img width="963" height="468" alt="image" src="https://github.com/user-attachments/assets/fb978003-eecb-42bd-bedb-ac860f8a4ec7" />

5.  Enter the Jupyter Lab tab in Codio and open the
    “CRUD_Python_Module.py” file and the “ProjectOneTestScript.ipynb”
    file.

<img width="975" height="217" alt="image" src="https://github.com/user-attachments/assets/cbd5d955-1fcd-474b-92a9-c17636ab106e" />

<img width="975" height="217" alt="image" src="https://github.com/user-attachments/assets/1dda0bd7-030f-42f2-99c8-ca94b70bcd1f" />

6.  Update the USER and PASS values in the \_\_init\_\_ method inside
    the “CRUD_Python_Module.py” file to match the username and password
    set in Step 4.

<img width="975" height="343" alt="image" src="https://github.com/user-attachments/assets/027208a5-5462-422f-9483-48a0b00cbad6" />

7.  In the “ProjectOneTestScript.ipynb” file, adjust the create and/or
    query values as desired, then select the desired test cell to run,
    then click the Play button at the top of the tab to test the various
    CRUD functionalities by section. Note that sections should be run
    sequentially, and after each press of the Play button, a test in a
    cell is ran, and the following cell is selected automatically, where
    the user can then press Play again to continue running additional
    test cells.

<img width="975" height="214" alt="image" src="https://github.com/user-attachments/assets/2cdf4373-9ba4-429e-8142-e8ccab151c8f" />

## Installation

1.  Codio

    1.  This README assumes users are using this project with Codio.

    2.  Installation: enroll in CS 340 at SNHU, access by clicking on
        the “Codio Learning Environment” option in Brightspace.

2.  MongoDB (Codio)

    1.  Already installed on Codio for CS 340 students, accessible via
        the Terminal tab.

3.  Python (Codio)

    1.  Already installed on Codio for CS 340 students, accessible via
        the Jupyter Lab tab.

4.  MongoDB (Optional, if not using Codio)

    1.  This README assumes users are using MongoDB via Codio, but this
        project can be used outside of Codio by installing Python
        locally through the following guide:

        1.  <https://www.mongodb.com/docs/manual/installation/>

5.  Python (Optional, if not using Codio)

    1.  This README assumes users are using Python via Codio, but this
        project can be used outside of Codio by installing Python
        locally through the following guide:

        1.  <https://wiki.python.org/moin/BeginnersGuide/Download>

## Usage of the Python CRUD Module

This project is primarily interacted with via the Python module. Code
examples, tests, and screenshots provided below.

### Code Examples

> Importing the module and instantiating the class:
>
> from CRUD_Python_Module import AnimalShelter
>
> animal_shelter = AnimalShelter()
>
> Example entry for a new animal record:
>
> animal_data = {
>
> "rec_num": 123,
>
> "age_upon_outcome": "2 years",
>
> "animal_id": "A58282612",
>
> "animal_type": "Dog",
>
> "breed": "Beagle",
>
> "color": "Tricolor",
>
> "date_of_birth": "2005-08-26",
>
> "datetime": "2015-08-18 11:11:00",
>
> "monthyear": "2015-08-18T11:11:00",
>
> "name": "Charlie",
>
> "outcome_subtype": "",
>
> "outcome_type": "Return to Owner",
>
> "sex_upon_outcome": "Neutered Male",
>
> "location_lat": 30.336163516779,
>
> "location_long": -97.4507799807501,
>
> "age_upon_outcome_in_weeks": 123
>
> }
>
> \# Using the create method to create new entries
>
> animal_shelter.create(animal_data)
>
> \# Using the read function to query existing entries
>
> animal_shelter.read(query)
>
> \# Using the update function to query existing entries, then update
> data for those entries:
>
> update_data = {"\$set": {"name": "Rover"}}
>
> animal_shelter.update(query, update_data)
>
> \# Using the delete function to query existing entries and delete
> matching entries
>
> animal_shelter.delete(query)

### Tests

> Inside of Codio, open the Jupyter Lab tab, then open the
> “ProjectOneTestScript.ipynb” file, which contains tests for creating a
> new entry and reading existing entries. Click the Play button (circled
> in red, item 4 in the image below) to run each test in this ipynb
> file.
>
<img width="975" height="477" alt="image" src="https://github.com/user-attachments/assets/f57f97a9-66f2-49a2-a0c7-c428715b4cb5" />
>
> The output of each test cell (example cell circled in red, item 1)
> appears below each cell and displays the outcome of the test (example
> cell circled in red, item 2).
>
<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/3a59c21a-e727-4407-a4cb-69f3d97aecd0" />

### Screenshots

Test output when creating a new entry for the Animal Shelter database:

<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/e83a5c0e-c907-40f1-aaaf-892ebca3eedf" />

Test output querying/reading existing entries in the database:

<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/454e3bee-a178-4f24-a2c5-48947bc539e2" />

Test output updating existing entries in the database:

<img width="975" height="479" alt="image" src="https://github.com/user-attachments/assets/ec251f15-ca7a-44c1-8bd5-3d40badb0e58" />

Test output updating existing entries in the database:

<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/f38f01b4-847b-45a3-83df-025a0202073f" />

## Challenges

Development of this project went smoothly, with only two major
challenges standing out: indention-based errors and the requirement to
have each screenshot of the dashboard “contain the Grazioso Salvare logo
and your unique identifier.”

At various points in development, I encountered errors related to
indention matching, caused by me moving various sections of code to new
lines to ensure lines are less than the maximum width of 79 characters
as set by [PEP
8](https://peps.python.org/pep-0008/#maximum-line-length). These errors
sometimes cascaded far past the point where the actual error occurred,
making it very difficult to track down where the actual error occurred.

The final challenge was related to the requirement of having the have
each screenshot of the dashboard “contain the Grazioso Salvare logo and
your unique identifier”, due to the large size of the client’s logo, and
the given project code’s handling of it. To overcome this, I scaled down
the size of the image in the app.layout section, like so:

html.Center(html.Img(

src='data:image/png;base64,{}'.format(encoded_image.decode()),

style={'width': '7%', 'height': 'auto'}

))

## Contact

Samuel Neblett

<samuel.neblett@snhu.edu>
