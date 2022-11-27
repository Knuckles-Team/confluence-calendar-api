# Confluence Calendar API
*Version: 0.1.0*

Confluence Calendar API Python Wrapper

### API Calls:
- Get Calendars
- Add Event

### Usage:
```python
#!/usr/bin/python
# coding: utf-8
import confluence_calendar_api

username = "<CONFLUENCE USERNAME>"
password = "<CONFLUENCE PASSWORD>"
confluence_url = "<CONFLUENCE URL>"
client = confluence_calendar_api.Api(url=confluence_url, username=username, password=password)

calendar = client.get_calendars(sub_calendar_id=12341)
print(calendar)
```

#### Install Instructions
Install Python Package

```bash
python -m pip install gitlab-api
```

#### Build Instructions
Build Python Package

```bash
sudo chmod +x ./*.py
pip install .
python setup.py bdist_wheel --universal
# Test Pypi
twine upload --repository-url https://test.pypi.org/legacy/ dist/* --verbose -u "Username" -p "Password"
# Prod Pypi
twine upload dist/* --verbose -u "Username" -p "Password"
```
