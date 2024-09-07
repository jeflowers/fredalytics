# Fredalytics

## Overview

`Fredalytics` is a combined repository that includes two separate Python projects designed to simplify the process of interacting with the Federal Reserve Economic Data (FRED) API:

1. **fredfpi** - Formerly `fred-api-wrapper`: A Python wrapper for the FRED API that simplifies the process of fetching economic data series, historical data, categories, and releases.
2. **fredapi-sig** - A project with its own specialized functionalities to interact with the FRED API.

## Subfolders

### 1. fredfpi

This folder contains the `fred-api-wrapper` project, which provides a Python wrapper for the Federal Reserve Economic Data (FRED) API.

#### Features

- Easy-to-use Python interface for FRED API
- Support for fetching series data, historical data, categories, and releases
- Built-in token verification for enhanced security
- Customizable error handling

#### Installation

To install the `fred-api-wrapper`, run the following command:

```bash
pip install fred-api-wrapper
```

#### Usage

Here's a quick example of how to use the `fred-api-wrapper`:

```python
from fred_api_wrapper import FredPyAPI

# Initialize the API with your token
fred_api = FredPyAPI("your_api_key_here")

# Get series data
gdp_data = fred_api.get_series_data("GDP")

# Get historical data
historical_gdp = fred_api.get_historical_data("GDP", observation_start="2020-01-01", observation_end="2023-12-31")

# Get categories
main_categories = fred_api.get_categories()

# Get releases
recent_releases = fred_api.get_releases(realtime_start="2023-01-01")

print(gdp_data)
print(historical_gdp)
print(main_categories)
print(recent_releases)
```

#### API Reference

The main class for interacting with the FRED API is `FredPyAPI`.

For detailed information on each method, please refer to the [FRED API documentation](https://fred.stlouisfed.org/docs/api/fred/).

### 2. fredapi-sig

This folder contains the `fredapi-sig` project, which is another Python project designed for specific interactions with the FRED API.

#### Features

- Custom implementations for interacting with the FRED API
- Additional tools and utilities specific to the project's goals

#### Installation and Usage

Please refer to the `README.md` file in the `fredapi-sig` folder for more detailed instructions on installation and usage.

## Contributing

Contributions to both sub-projects (`fredfpi` and `fredapi-sig`) are welcome! Please refer to the respective `CONTRIBUTING.md` files in each subfolder for guidelines on how to contribute to these projects.

## License

This combined repository is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- Federal Reserve Bank of St. Louis for providing the FRED API
- All contributors to both `fredfpi` and `fredapi-sig` projects

## Contact

For any questions or concerns, please open an issue on the GitHub repository.
