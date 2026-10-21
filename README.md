# Subject night day plot

Subject night day plot

## What it does

| Step | What it does |
|---|---|
| **Connect to EarthRanger** |  |
| **Set Time Range** | Choose the period of time to analyze. |
| **Subject Group** | Get observations for a subject group from EarthRanger. |
| **Process Relocations** |  |
| **Classify Is Night** | Classifies if segments occur at night in a trajectory dataframe |
| **Persist Relocations** | Persist dataframe to a file or cloud storage object. |
| **Relocations To Trajectory** |  |
| **Persist Trajectories** | Persist dataframe to a file or cloud storage object. |
| **Map Trajectory Columns** | Maps and transforms the columns of a DataFrame based on the provided parameters. The order of the operations is as follows: drop columns, retain/reorder columns, and rename columns. |
| **Sort Night Day Values** |  |
| **Extract Date from Segment Start** | Decompose a datetime column into its constituent temporal components. |
| **Set Groupers** |  |
| **Split Groups** |  |
| **Summarize Night Day Df** |  |
| **Persist Night Day Df** | Persist dataframe to a file or cloud storage object. |
| **Map Night Day DF** | Maps and transforms the columns of a DataFrame based on the provided parameters. The order of the operations is as follows: drop columns, retain/reorder columns, and rename columns. |
| **Draw Night Day Line Chart** | Generates a line chart from the provided params |
| **Draw Night Day Table** | Creates an HTML table of the provided dataframe. |
| **Persist Night Day Line Chart** | Persist text to a file or cloud storage object. |
| **Create Plot Widget Single View** | Create a plot widget with a single view. |
| **Persist Night Day Table as HTML** | Persist text to a file or cloud storage object. |
| **Create Table Widget Single View** | Create a table widget with a single view. |
| **Merge Widget Views** | Merge widgets with the same `title` and `widget_type`. |
| **Set Workflow Details** | Add information that will help to differentiate this workflow from another. |
| **Merge Widget Views** | Merge widgets with the same `title` and `widget_type`. |
| **Gather Dashboard** |  |

## Requirements

- Access to a **EarthRanger** data source, set up as a connection

---

## 1. Load the Workflow

In the workflow runner, add a new template using this repository's URL. Once added, select
**Subject night day plot** from the available templates list to load it.

---

## 2. Configure the Workflow

You'll be prompted to fill in the following parameters before running.

### Connect to EarthRanger

| Field | Description | Default |
|---|---|---|
| Data source *(required)* | Select one of your configured data sources. | — |

### Set Time Range

| Field | Description | Default |
|---|---|---|
| Since *(required)* | The start time | — |
| Until *(required)* | The end time | — |
| Timezone |  | — |

### Subject Group

| Field | Description | Default |
|---|---|---|
| Subject Group Name *(required)* | ⚠️ The use of a group with mixed subtypes could lead to unexpected results | — |

### Set Groupers

| Field | Description | Default |
|---|---|---|
|   |             Specify how the data should be grouped to create the views for your dashboard.             This field is optional; if left blank, all the data will appear in a single view.              | — |

### Set Workflow Details

| Field | Description | Default |
|---|---|---|
| Workflow Name *(required)* |  | — |

---

## Developing

```bash
# recompile spec.yaml (first time: --install; after that: --update, which bumps VERSION.yaml)
./dev/recompile.sh --update

# run the test cases in test-cases.yaml
pixi run --manifest-path pixi.toml -e default bash dev/pytest-cli.sh subject_day_night_location_map_2 --all
```

Documentation: [docs/index.html](docs/index.html).
