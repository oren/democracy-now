# Senate API

## Usage
```
curl https://lda.senate.gov/api/v1/ | jq '.'

{
  "constants/contribution/itemtypes": "https://lda.senate.gov/api/v1/constants/contribution/itemtypes/",
  "constants/lobbyist/suffixes": "https://lda.senate.gov/api/v1/constants/lobbyist/suffixes/",
  "constants/lobbyist/prefixes": "https://lda.senate.gov/api/v1/constants/lobbyist/prefixes/",
  "constants/general/states": "https://lda.senate.gov/api/v1/constants/general/states/",
  "constants/general/countries": "https://lda.senate.gov/api/v1/constants/general/countries/",
  "filings": "https://lda.senate.gov/api/v1/filings/",
  "contributions": "https://lda.senate.gov/api/v1/contributions/",
  "registrants": "https://lda.senate.gov/api/v1/registrants/",
  "clients": "https://lda.senate.gov/api/v1/clients/",
  "lobbyists": "https://lda.senate.gov/api/v1/lobbyists/",
  "constants/filing/filingtypes": "https://lda.senate.gov/api/v1/constants/filing/filingtypes/",
  "constants/filing/lobbyingactivityissues": "https://lda.senate.gov/api/v1/constants/filing/lobbyingactivityissues/",
  "constants/filing/governmententities": "https://lda.senate.gov/api/v1/constants/filing/governmententities/"
}
```

With authentication key:
```
curl https://api.congress.gov/v3/bill/117/hr/3076?api_key=xxx
```


Notes:
* https://lda.senate.gov/api/redoc/v1/#section/About-the-REST-API/Changes

Using the python client
```
./cdg_cli --prompt-key

./cdg_cli bill/117/hr/21/committees

  INFO     __main__/main:111 HTTP Status: 200
  INFO     __main__/main:112 API Returned:
{'committees': [{'activities': [{'date': '2021-01-07T01:26:34Z',
                                 'name': 'Referred to'}],
                 'chamber': 'Senate',
                 'name': 'Homeland Security and Governmental Affairs Committee',
                 'systemCode': 'ssga00',
                 'type': 'Standing',
                 'url': 'https://api.congress.gov/v3/committee/senate/ssga00?format=json'},
                {'activities': [{'date': '2021-01-04T15:11:25Z',
                                 'name': 'Referred to'}],
                 'chamber': 'House',
                 'name': 'Oversight and Reform Committee',
                 'systemCode': 'hsgo00',
                 'type': 'Standing',
                 'url': 'https://api.congress.gov/v3/committee/house/hsgo00?format=json'}],
 'request': {'billNumber': '21',
             'billType': 'hr',
             'billUrl': 'https://api.data.gov/congress/v3/bill/117/hr/21?format=json',
             'congress': '117',
             'contentType': 'application/json',
             'format': 'json'}
}
```

## Documentation
* API: https://api.congress.gov/
* CLI: https://github.com/LibraryOfCongress/api.congress.gov
