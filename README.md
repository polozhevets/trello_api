# trello_api
Trello API Client

Python2 and Python3 supported

## Install

```bash
pip install git+https://github.com/polozhevets/trello_api
```

## Auth

#### TRELLO_APP_KEY: https://trello.com/app-key/
#### TRELLO_APP_TOKEN:

First you need gen auth url:
```python
from trello_api import TrelloApi

trello_app = TrelloApi(TRELLO_APP_KEY)

token_url = trello_app.get_token_url('MyAppBot', expires='never', write_access=True)
```
Than you need copy value of token_url and auth your trello account in webbrowser
After that you will get token

#### Apply token in your app:
```python
trello_app.set_token(TRELLO_APP_TOKEN)
```

Deprecated source: https://developers.kilnhg.com/Code/Trello/Group/TrelloPy?nr=
