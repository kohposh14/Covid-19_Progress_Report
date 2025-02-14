# COVID-19 Vaccination Progress Analysis

## Project Overview
A data analysis project examining global vaccination efforts using Python and Plotly visualizations. This project helps understand:
- Vaccine distribution by country
- Vaccination rates per hundred people
- Daily vaccination trends
- Comparison of vaccine types used globally

## Key Features
```python
# Core Analysis Performed
1. Data aggregation by country and vaccine type:
   country_vaccine = data_df.groupby(["country", "iso_code", "vaccines"]).max()

2. Vaccine-type analysis:
   for v in vaccines:
       print(f"Countries using {v}: {list(countries)}")

3. Interactive geographical visualization:
   px.choropleth(country_vaccine, 
                locations="iso_code",
                color="Vaccines",
                hover_name="Country",
                title="Global Vaccine Distribution")
```

## Key Insights
- **Vaccine Diversity**: Countries use 2-9 different vaccines (e.g., Iran uses 9 types including COVIran Barekat and SpikoGen)
- **Regional Trends**:
  - Oxford/AstraZeneca dominates in African nations
  - mRNA vaccines (Pfizer/Moderna) prevail in North America/Europe
  - China uses 5 domestic vaccines including Sinopharm and ZF2001
- **Vaccination Coverage**:
  - Analyze `people_fully_vaccinated_per_hundred` for herd immunity progress
  - Compare `daily_vaccinations_per_million` between nations


## Python Libraries Used:
- Pandas & NumPy - Data manipulation and aggregation
- Matplotlib & Seaborn - Statistical visualization
- Plotly - Interactive geographical mapping (choropleth) and dynamic visualizations


## Future Enhancements
- Add time-series analysis of vaccination rollout phases
- Implement vaccine effectiveness comparison metrics
- Create forecasting model for herd immunity timelines
- Build interactive dashboard with Dropdown filters

---

## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Authors

- [@octokatherine](https://www.github.com/octokatherine)


## API Reference

#### Get all items

```http
  GET /api/items
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### Get item

```http
  GET /api/items/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### add(num1, num2)

Takes two numbers and returns the sum.


## Running Tests

To run tests, run the following command

```bash
  npm run test
```

