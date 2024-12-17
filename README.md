# SyncAll

This is a video calling web app that uses the Agora SDK with a Django backend. Built for CMSC 447.

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/smeed03/SyncAll
    cd SyncAll
    ```

2. Set up the Python virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the Python dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Update Agora credentials
    Head to agora.io, create an account, then create an app. From that app, retrieve the appid and appCertificate and update these credentials in views.py and streams.js accordingly.

    In views.py:
    ```sh
    def getToken(request):
      appId = "YOUR APP ID"
      appCertificate = "YOUR APPS CERTIFICATE"
    ......
    ```
    In streams.js:
    ```sh
    ....
    const APP_ID = 'YOUR APP ID'
    ....
    ```
    
5. Run server
    ```sh
    python manage.py runserver
    ```
