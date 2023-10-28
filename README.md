# TecheEmmisions</br>
●	Project summary </br>
○	The issue we are hoping to solve</br>
○	How our technology solution can help</br>
○	Our idea</br>
●	Technology implementation</br> 
○	IBM AI service(s) used</br>
○	Other IBM technology used</br>
○	Solution architecture</br>
●	Presentation materials</br>
○	Solution demo video </br>
○	Project development roadmap </br>
●	Additional details</br>
○	How to run the project</br>
○	Live demo</br>
●	About this template</br>
○	Contributing</br>
○	Versioning</br>
○	Authors</br>
○	License(MIT)</br>
○	Acknowledgments</br>

















Project Summary</br>
The Issue we are hoping to solve</br>
For our standard desktop PC and screen, operated over a six-year period, the annual GHG impact (aka carbon footprint, CFP) will be around 778kg CO2e.Based on supplier data for PC models used extensively within the University, scaled to use over a six-year period, the carbon footprints of some typical working setups are:</br>
●	Desktop + screen: 621kg CO2e</br>
●	Laptop* + screen: 691kg CO2e (+11%)</br>
●	Desktop + 2 screens: 903kg CO2e (+45%)</br>
●	Laptop* + screen at office + screen at home: 928kg CO2e (+49%)</br>
●	Desktop + screen + laptop*: 1,030kg CO2e (+66%)</br>
●	Sample PC kept 'active' continuously: 73kg CO2e</br>
●	With default power saving features: 37kg CO2e (-49%)</br>
●	Shutdown when not in use: 17.6kg CO2e (-76%)</br>
●	Turned off at wall when not in use: 14.7kg CO2e (-80%)</br>
Not only this but Video Gaming Machines, Crypto Mining Rigs, Massive Central Servers to Embodied Carbon(CO2 produced during manufacturing, using and disposal of electronic devices or components) is huge and growing by all means. Leaving a gigantic issue to be addressed and resolved.</br>
How our technology solution can help</br>
Our Solution CodeCarbon analyzes and detects the different factors which help in estimating the carbon footprint of electronic devices and suggest how to reduce it using technologically advanced solutions and well solutions based on conservative approaches.</br>
Our Idea</br>
CodeCarbon estimates and tracks carbon emissions from electronic devices, quantifying and analyzing their impact. We found some global data like "computing currently represents roughly 0.5% of the world’s energy consumption" but nothing on our individual/organization level impact. At CodeCarbon, we believe, along with Niels Bohr, that "Nothing exists until it is measured". So we found a way to estimate how much CO2 we produce while running our code.</br>
How?</br>
We created a Python package that estimates your hardware electricity power consumption (GPU + CPU + RAM) and we apply to it the carbon intensity of the region where the computing is done.</br>
 
We explain more about this calculation in the following section of the documentation.</br>
Our hope is that this package will be used widely for estimating the carbon footprint of computing, and for establishing best practices with regards to the disclosure and reduction of this footprint.</br>
Calculations:</br>
Carbon dioxide (CO₂) emissions, expressed as kilograms of CO₂-equivalents [CO₂eq], are the product of two main factors :</br>
C = Carbon Intensity of the electricity consumed for computation: quantified as g of CO₂ emitted per kilowatt-hour of electricity.</br>
E = Energy Consumed by the computational infrastructure: quantified as kilowatt-hours.</br>
Carbon dioxide emissions (CO₂eq) can then be calculated as C * E </br>
Carbon Intensity of the consumed electricity is calculated as a weighted average of the emissions from the different energy sources that are used to generate electricity, including fossil fuels and renewables. In this toolkit, the fossil fuels coal, petroleum, and natural gas are associated with specific carbon intensities: a known amount of carbon dioxide is emitted for each kilowatt-hour of electricity generated. Renewable or low-carbon fuels include solar power, hydroelectricity, biomass, geothermal, and more. The nearby energy grid contains a mixture of fossil fuels and low-carbon energy sources, called the Energy Mix. Based on the mix of energy sources in the local grid, this package calculates the Carbon Intensity of the electricity consumed.</br>
                          
When available, CodeCarbon uses global carbon intensity of electricity per cloud provider ( here ) or per country ( here ). If we don’t have the global carbon intensity or electricity of a country, but we have its electricity mix, we compute the carbon intensity of electricity using this table:</br>
S.No:	Energy Source	Carbon Intensity(Kg/MWh)</br>
1	Coal 	995</br>
2	Petroleum	816</br>
3	Natural Gas	743</br>
4	GeoThermal	38</br>
5	Hydroelectric	26</br>
6	Nuclear	29</br>
7	Solar	48</br>
8	Wind	26</br>
Sources: 1. for fossil energies 2. for renewables energies</br>
Then, for example, if the Energy Mix of the Grid Electricity is 25% Coal, 35% Petroleum, 26% Natural Gas and 14% Nuclear:</br>
Net Carbon Intensity = 0.25 * 995 + 0.35 * 816 + 0.26 * 743 + 0.14 * 29 = 731.59         kgCO₂/kWh</br>
If ever we have neither the global carbon intensity of a country nor its electricity mix, we apply a world average of 475 gCO2.eq/KWh ( source ).</br>

Technology Implementation</br>
IBM AI service(s) that can be used</br>
1.	AI Factsheets - Included with Cloud Pak for Data - Used to organize and track lineage events, facts, and details for each of our machine learning model’s lifecycle and increase transparency for model governance needs.</br>
2.	IBM Match 360 with Watson - Included with Cloud Pak for Data - Builds 360-degree view of our customers by matching data from disparate sources to create a single, complete, and trusted version of the truth.</br>
3.	Watson Machine learning - Included with Cloud pak for Data -  Builds and trains machine learning models with tools for all skill levels. Deploy and manage models at scale.</br>
4.	Watson OpenScale - Included with Cloud Pak for Data - Infuses AI with trust and transparency. Understands how AI models make decisions to detect and mitigate bias.</br>
5.	Watson Studio - Included with Cloud Pak for Data - Unleashes the power of your data, Builds custom models and infuses your business with AI and machine learning.</br>
Type of data</br>
-	Tabular data in delimited files or relational data in remote data sources</br>
-	Image files</br>
-	Textual (unstructured) data in documents</br>
Type of tasks to be done</br>
-	Prepare data: cleanse, shape, visualize, organize and validate data.</br>
-	Analyze data: identify patterns and relationships in data and display insights</br>
-	Build models: build, train, test, and deploy models to make predictions or optimize decisions.</br>
Automation required</br>
-	Code editor tools: Used to write code in Python, R or also spark</br>
-	Graphical builder tools: Use menus and drag and drop functionally on a builder to visually program</br>
-	Automated builder tools: Used to configure automated tasks that require limited user input.</br>

Right tools used (Tabular or relational data).</br>
-	Jupyter notebook editor [code editor]{Prepare & Analyze data, Build models}</br>
Use the Jupyter notebook editor to create a notebook in which you run code to prepare, visualize, and analyze data, or build and train a model.</br>
Data format</br>
Any</br>
Data size</br>
Any</br>
How you can prepare data, analyze data, or build models</br>
Write code in Python or R, all also with Spark.</br>
Include rich text and media with your code.</br>
Work with any kind of data in any way you want.</br>
Use preinstalled or install other open source and IBM libraries and packages.</br>
Schedule runs of your code</br>
Import a notebook from a file or a URL.</br>
Share read-only copies of your notebook externally.</br>
Get started</br>
To create a notebook, click New asset > Jupyter notebook editor.</br>
Learn more</br>
Documentation about notebooks</br>

-	JupyterLab [code editor]{Prepare & Analyze data, Build models}</br>
Use the JupyterLab IDE to create a notebook or Python script in which you run code to prepare, visualize, and analyze data, or build and train a model. JupyterLab is integrated with a Git repository which must be associated with the project.</br>
Data format</br>
Any</br>
Data size</br>
Any</br>
How you can prepare data, analyze data, or build models</br>
Write code in Python.</br>
Include rich text and media with your code.</br>
Work with any kind of data in any way you want.</br>
Use preinstalled or install other open source and IBM libraries and packages.</br>
Import a notebook from a file.</br>
Share your notebook or script in a Git repository.</br>
Get started</br>
To use JupyterLab, click Launch IDE > JupyterLab.</br>
Learn more</br>
Documentation about JupyterLab</br>

-	Decision Optimization model builder [Graphical builder and code editor]{Prepare data, Build models}</br>
Use Decision Optimization to build and run optimization models in the Decision Optimization modeler or in a Jupyter notebook.</br>
Required service</br>
Decision Optimization</br>
Data formats</br>
Tabular: CSV files</br>
Data size</br>
Any</br>
How you can prepare data</br>
Import relevant data into a scenario and edit it.</br>
How you can build models</br>
Build prescriptive decision optimization models.</br>
Create, import and edit models in Python DOcplex, OPL or with natural language expressions.</br>
Create, import and edit models in notebooks.</br>
How you can solve models</br>
Run and solve decision optimization models using CPLEX engines.</br>
Investigate and compare solutions for multiple scenarios.</br>
Create tables, charts and notes to visualize data and solutions for one or more scenarios.</br>
Get started</br>
To create a Decision Optimization model, click New asset > Decision Optimization, or for notebooks click New asset > Jupyter notebook editor.</br>
Learn more</br>
Documentation about Decision Optimization</br>

-	IBM Match 360 with Watson [Automated builder]{Prepare data</br>}
Use IBM Match 360 with Watson to create master data entities that represent digital twins of your customers. Model and map your data, then run the matching algorithm to create master data entities. Customize and tune your matching algorithm to meet your organization's requirements.</br>
Required services</br>
IBM Match 360 with Watson IBM Watson Knowledge Catalog</br>
Data size</br>
Any</br>
How you can prepare data</br>
Model and map data from sources across your organization.</br>
Run the customizable matching algorithm to create master data entities.</br>
View and edit master data entities and their associated records.</br>
Get started</br>
To create an IBM Match 360 configuration asset, click New asset > Master data configuration.</br>
Learn more</br>
Documentation about IBM Match 360 with Watson</br>

-	Dashboard editor [Graphical builder]{Analyze data}</br>
Use the Dashboard editor to create a set of visualizations of analytical results on a graphical builder.</br>
Required service</br>
Cognos Dashboard</br>
Data format</br>
Tabular: CSV files</br>
Relational: Tables in some relational data sources</br>
Data size</br>
Any size</br>
How you can analyze data</br>
Create graphs without coding.</br>
Include text, media, web pages, images, and shapes in your dashboard.</br>
Get started</br>
To create a dashboard, click New asset > Dashboard editor. The Dashboard editor tile is in the Graphical builders section.</br>
Learn more</br>
Documentation about dashboards</br>

-	Watson Pipelines [Graphical builder]{Prepare and Analyze data, Build models}</br>
Use the Pipelines canvas editor to create a flow to prepare, visualize, and analyze data, or build and train a model.</br>
Required service</br>
Watson Knowledge Catalog or Watson Studio</br>
Data format</br>
Any</br>
Data size</br>
Any</br>
How you can prepare data, analyze data, or build models</br>
Use a variety of nodes that each contain their own logs.</br>
Incorporate notebooks into the flow to run any Python or R code.</br>
Work with any kind of data in any way you want.</br>
Schedule runs of your flow.</br>
Import data from your mounted PVC, project, or ingest data from Github.</br>
Create your custom component with a Python code.</br>
Conditionalize your pipelines to monitor data quality however you want.</br>
Use webhook to send emails or messages to keep up to date on the status of your flow.</br>
Get started</br>
To create a new pipeline, click New asset > Pipelines.</br>
Parent topic: Projects</br>





Other IBM technology used</br>
1.	Nodered</br>






Solution Architecture</br>

Reference</br>
 


 







Presentation materials</br>
Solution demo video</br>




Project development roadmap</br>
 


















Additional details</br>
How to run the project</br>
1:     pip install codecarbon</br>
2:    conda install -c conda-forge codecarbon</br>
3:    pip install codecarbon</br>
4:    conda install -c codecarbon -c conda-forge codecarbon</br>
5:    conda create --name codecarbon</br>

6:    conda activate codecarbon</br>

7:    codecarbon init </br>
8 :   conda install -c codecarbon -c conda-forge codecarbon</br>
9:    codecarbon init </br>
10 : codecarbon monitor</br>


Live demo</br>



We are developing Project CodeCarbon to analyze and estimate the carbon content and  emissions from technological devices and systems.</br>

Much as technology has seeped into all aspects of our lives, the costs that come with the use of these devices is growing exponentially. To add context, carbon emissions from devices and systems is</br> 



Licence: MIT</br>














