# RailwagonLocation

![GitHub top language](https://img.shields.io/github/languages/top/Odya-LLC/flask_html)
![LICENCE](https://img.shields.io/github/license/Odya-LLC/railwagonlocation)
![Odya](https://img.shields.io/static/v1?label=Developed_by&message=Odya&color=green&logo=python)

Python client for the RailwagonLocation API.


## Installation

```bash
pip install railwagonlocation
```

## Usage

```python
from railwagonlocation import RailWagonLocation

# Create client
# username - username for RailwagonLocation API
# password - password for RailwagonLocation API
# base_url - base url for RailwagonLocation API
# return_format - json or xml, default json
client = RailWagonLocation('username', 'password', 'base_url',return_format='json',)

# Get wagon info
wagons = client.get_wagon_info('12345678')
# Get wagon repair s history
history = client.get_wagon_repair_history('12345678')
# Get vagon info with history
wagon_history = client.get_wagon_history('12345678',days_limit=30)

# Get all wagon info
# all_operations - get all operations for wagon
# added_last_minutes - get wagons added in last minutes without calendar_date
# calendar_date - get wagons added in calendar_date, added_last_minutes not work with calendar_date
wagons = client.get_all_wagons_info(all_operations=True, added_last_minutes=60, calendar_date="2021-01-01")

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License (see the LICENSE file for details).