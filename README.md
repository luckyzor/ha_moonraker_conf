# Home Assistant configuration to integrate Klipper API (Moonraker)

## Here the example of my Dashboard:
![Alt text](print_screens/dashboard_example.png?raw=true "Dashboard Example")

## Dashboard raw configuration
   - lovelace-dashboard/printer_dashboard.yaml

## Main configuration
   - moonraker.yaml  
     (Change the IP of the printer in all the URL links and change the printer name (**tip**: you can replace all "vcore400" by "ender3pro" with vscode,for example)

## How to configure the Thumbnail Cam and a PI Cam(if you have any)
   - Thumbnail CAM should be added in integrations -> Generic Camera  
     Change the IP of your printer  
     URL: `http://10.0.0.8:7125/server/files/gcodes/{{ states('sensor.vcore400_url_thumbnail') }}`  
     Authentication -> Basic
     the rest keep it default

   - RaspBerryPi CAM should be added in integrations -> MJPEG IP CAMERA  
     Change the IP of your printer  
     MJPEG URL: `http://10.0.0.8/webcam/?action=stream`  
     Still image URL: `http://10.0.0.8/webcam/?action=snapshot`  
     the rest keep it default

#### Here you can find more information about Moonraker API: https://moonraker.readthedocs.io/en/latest/web_api/

#### Feel free to open and issue if you have any question or if something doens't work
