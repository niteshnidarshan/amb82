# amb82
Arduino

step1: connect amb82-mini with CH34C port on laptop

step2: open Arduino IDE 2.2.1

step3: go to prefrence and add below library:

  https://github.com/ambiot/ambpro2_arduino/raw/main/Arduino_package/package_realtek.com_amebapro2_index.json

  **Error scenario during library update**

  If you get time out error during this json library update, it may because of below issue:

  Sometime internet service provider configures your wifi with thier default DNS address which restricts some of the sites. Due to this Arduino IDE tries to update this library but it is blocked. To resolve this issue do the below steps:

  step3.1: Go to Wifi prefrence and click on 'i' or details/ configuration of wifi.
  
  step3.2: update DNS address IPv4 with 1.1.1.1 and save then restart laptop.

  It will resolve the timeout error and the json library will be updated.
  

step4: press ok then go to board manager and search for ameba/ amb 
  If it is not showing any boards in the list then follow below steps

  **AMB82-mini initially does not work with Arduino IDE 2.2.x**

    step 4.1: uninstall Arduino IDE 2.2.1 and install Arduino IDE 1.8.19
    step 4.2: follow step3 and step4
    step 4.3: once found Realtek AMB 82- mini board - select and install
    step 4.4: after installing board, you can continue with this IDE or you can install Arduino IDE 2.2.1 - now it will search the borad.

step5: select appropriate board then select port

**Error Scenario [arduino ide compilation error]**
  
  While compile/ upload code to AMB82, if console return some error like: 
    
  **ino_validation_macos: permission denied**

  Follow below steps to resolve this error:
  
    Step5.1: Go to Board Manager and search for the board- Ameba/ amb
    
    Step5.2: Change the installed version to 4.0.4-1

    
    This version will allow you to compile and upload your code to AMB82 board.

    

