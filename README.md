# iv2021-M*yb*nk Assessment
> **Language** = HTML, CSS, Javascript (jQuery & AJAX) <br />
> **Front-end** = Bootstrap, chartJS, leafletJs <br /> 
> **Back end/API** = nodeJS (npm package called `json-server` as fake API) & real-time API`https://api.wheretheiss.at/` <br /> 


## Installation Guide
**For front-end:** <br /> 
> [1] Go to your local server directory (httpdocs dir for XAMPP) <br /> 
> [2] Open terminal/git bash and type `git clone https://github.com/syukranDev/iv2021_syukran.git` <br /> 
> [3] Fire up your local server. <br /> 

**For back-end (Assuming you have nodejs installed):** <br /> 
> [1] Go to path `iv2021_syukran/fakeAPI` and delete all files except `db.json` and make a copy of it to desktop (will use later in step 5) <br />
> [2] Open terminal in `iv2021_syukran/fakeAPI` directory and type `npm install -D json-server` <br />
> [3] Run the fakeAPI server by `json-server --watch db.json`, this if all good, your JSON server will be running at port 3000 (http://localhost:3000) <br /> 
> [4] `node_modules` , `db.json`, `package.json`, `package-lock.json` will be generated. <br />
> [5] Replace the `db.json` generated by the JSON server with the `db.json` you copied to desktop. <br />


## Web Apps Homepage Explanation
**a) Window Tab 1 (Current ISS location) & 2 (ISS Trace Route) & 3 (Outside ISS Temperature)** <br />
> used self-generate data inside the `db.json`, all data shown in `db.json` is fetched (METHOD: GET) by jQuery/AJAX from `api-url: http://localhost:3000/Todos` of json-server. <br />

**b) Window Tab 4 (Embedded Tweet)** <br />
>Tweet ID is fetched manually by simply going to tweet url (https://twitter.com/username/status/tweetID). Planned to get new Twitter API token key to query (GET) the tweet ID, but application rejected. <br />

**c) Window Tab 4 (how-many-people-in-space)**  <br />
> Data is fetched (method: GET) directly from `https://api.wheretheiss.at/` 


![webpage full](https://user-images.githubusercontent.com/51852197/144365761-77372233-c657-4fe5-9b20-6651a8c09178.png)


## Remarks & Future Dev
-`json-server` is a full fake REST API used for quick backend prototyping,  more infos here: https://www.npmjs.com/package/json-server <br />
-`db.json` of fakeAPI (json-server) only contain 11 sets of self-generate data (lattitude,longitude,temperature,country,id,timestamp) due to simplicity testing, so there is no new data being updated into the `db.json`. <br />
![js pic](https://user-images.githubusercontent.com/51852197/144367245-cad431bb-6ad2-4091-8462-34f8130a9eb7.PNG) <br />
-**not really meet the main task objective due to time constraint & limited knowledge on DOM manipulation, but i think meet the Extension A,B,C.**



