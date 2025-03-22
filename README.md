## Connecting your Raspberry Pi Pico W to AWS IoT Core.
This is a proyect that I followed from the video [video](https://www.youtube.com/watch?v=DEBmpVPnZb0) from **Shilleh**.

# Step 1 : Configuring AWS IoT Core policies.
To be able to make a connection between the Raspberry Pi and AWS we have to create some policies that will allow the communication.
in the Policies option, go to the bottom of the page until Policy Document and create four new Statement.
* First statement: Allow iot:Connect for all resources (*)
* Second statement: Allow iot:Publish for all resources (*)
* Third statement: Allow iot:Receive for all resources (*)
* Fourth statement: Allow iot:Subscribe for all resources (*)

***This is not recommended for general use, but for this small project, it will be allowed.***

![image](https://github.com/user-attachments/assets/bbef2c6b-6200-4b91-9a04-5a75472d5a3d)

# Step 2 : Creating an AWS IoT things.
_A thing resource is a digital representation of a physical device or logical entity in AWS IoT/_

* Number of Things to Create: Select "Create a single thing" (first option).
* Create a Name: Use a meaningful name, usually "picow", then click Next.
* Device Certificate: Choose "Auto-generate a new certificate" (first option).
* Policy Selection: Select the policy you created earlier, then click "Create thing".

<ins>**Important Step: After clicking the "Create thing" button, a window will pop up on your screen displaying different certificates. You must download all of them to proceed with the configuration of your Raspberry Pi Pico W**</ins>


![image](https://github.com/user-attachments/assets/5ffe5d64-de35-45de-b9a1-f36c1b3eda58)

# Step 3 : Coding the scripts to connect the device with AWS IoT Core.


![image](https://github.com/user-attachments/assets/d9ef5eef-1538-4f9d-88b1-b257993fb362)
