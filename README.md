name: GetScreen Windows (6H)



on:

  workflow_dispatch:



jobs:

  build:

    runs-on: windows-latest



    steps:

      - name: Downloading & Setting Up

        run: |

         echo "EMAIL_SECRET=fniasonicexe@gmail.com" > secrets.txt

         Invoke-WebRequest -Uri "https://www.dropbox.com/scl/fi/gdzoens68gz1o4wuwtf0x/down.bat?rlkey=wd1ecn33dv9yn2uvdyynavbs6&dl=1" -OutFile "down.bat"

         cmd /c down.bat



      - name: Time Counter

        run: python time.py
