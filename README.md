# Wildlife Trafficking Choropleth Map (D3.js)

Interactive **choropleth map visualization** showing wildlife trafficking incidents around the world by year.

This project uses **D3.js** to visualize the number of incidents per country and allows users to explore the data through a **year dropdown and interactive tooltips**.

---

## Repository Structure

```
data/
   wildlife_trafficking.csv
   world_countries.json

lib/
   d3.v5.min.js
   d3-tip.min.js
   d3-geo-projection.v2.min.js
   d3-legend.min.js
   topojson.v2.min.js

index.html
README.md
```

---

## Dataset

### wildlife_trafficking.csv

Contains wildlife trafficking incident data.

Columns:

- **Year** — year the incident occurred  
- **Country** — country where the incident occurred  
- **Number_of_Incidents** — number of incidents reported  
- **Average_Fine** — average fine in USD  
- **Average_Imprisonment** — average imprisonment term (years)

---

### world_countries.json

GeoJSON file containing country shapes used to draw the world map.

---

## Visualization Features

### Choropleth Map

The map displays **wildlife trafficking incidents per country**.

- Countries are colored based on **number of incidents**
- Uses **4 color gradations**
- Darker color = more incidents
- Countries with **no data appear in gray**

---

### Year Selection

A dropdown menu allows the user to:

- Select a **year**
- Update the map dynamically based on the selected year

---

### Tooltip

Hovering over a country shows:

- Country name  
- Year  
- Number of incidents  
- Average fine (USD)  
- Average imprisonment (years)

Values for fine and imprisonment are **rounded to two decimal places**.

---

### Legend

A color legend shows the **four incident ranges** used to color the map.

The ranges are automatically calculated based on the **distribution of incidents for the selected year**.

---

## Running the Project Locally

Because browsers block loading CSV and JSON files locally, run a local server.

Start the server:

```powershell
python -m http.server 8000
```

Then open the visualization:

```
http://localhost:8000/index.html
```

Use **Google Chrome** for best compatibility.

---

## Technologies Used

- **D3.js v5**
- **D3 Tip (tooltips)**
- **TopoJSON**
- **D3 Geo Projection**
- HTML
- CSS
- JavaScript

