---
title: Deploy SAP HANA on Google Cloud
description: Deploy and configure your SAP HANA, express edition instance on Google Cloud in 10 minutes.
auto_validation: true
primary_tag: products>sap-hana
tags: [  tutorial>beginner, products>sap-hana, products>sap-hana\,-express-edition, products>sap-web-ide ]
time: 10
---

## Details
### You will learn  

**THIS TUTORIAL SERIES CAN ONLY BE EXECUTED WITH A LIVE INSTRUCTOR**  as it is.

To complete this tutorial, you will be using a virtual machine powered and sponsored by [Google Cloud](https://cloud.google.com/).

![Google Cloud Platform](gcpx2.png)


---

[ACCORDION-BEGIN [Step 1: ](Log into your test account)]

The experts at the Developer Garage at SAP TechEd will provide you with access details. Open a new **incognito window** using Google Chrome.

![Incognito Chrome](incognito.png)

And navigate to the Google Cloud launcher: `https://console.cloud.google.com/launcher`

![Incognito Chrome](incognito2.png)

Click **SIGN IN**.

![Log in to the Google Cloud launcher](signin.png)

And use the user name provided to you by the experts ...

![Log in to the Google Cloud launcher](1.png)

... and the password as provided to you by the experts.

![Log in to the Google Cloud launcher](2.png)

You will be presented with the terms and policies applied to the test account.

![Accept terms](accept.png)

Click **CONSOLE**.

![Click console](console.png)

Agree to the terms applicable to the test account.

![Agree to terms](agree.png)

Click **Select a project**.

![Select project](project.png)

You will find a pre-created project. Select it.

![Select project](project2.png)

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 2: ](Deploy SAP HANA, express on Google Cloud Platform)]

Look for the full image of SAP HANA, express edition on the Google Cloud Platform using the search bar on the top. Click on the result that includes **server + applications**.

![Look for SAP HANA](search.png)

Click **LAUNCH ON COMPUTE ENGINE**.

![Launch on compute engine](launch.png)

Change the name of the instance to `hxe`:

![Launch on compute engine](deploy0.png)

Scroll down to accept the terms of service and agree on sharing information (remember, this applies to the test account) and click **Deploy**.

![Launch on compute engine](deploy.png)

Wait until the instance is deployed and click on the name of the instance

![Configure VM](vm.png)

Click **Edit**

![Configure VM](edit.png)

Edit the network settings

![Configure VM](i1.png)

And choose **Create IP address**

![Configure VM](i2.png)

Call the IP address any name and choose **Reserve**

![Configure VM](i3.png)

Scroll down and click **Save**

![Configure VM](i4.png)

Go back and click  **SSH**.

![Launch SSH](ssh.png)

Copy and paste the following command into the console:

```txt
sudo su - hxeadm
```

And press **Enter**.

![Configure GCP](sudo.png)

You will be asked for some parameters to configure your SAP HANA, express edition instance.

![Configure GCP](config.png)

Configuration will take just a couple of minutes. In the meantime, continue with the next step.

[DONE]
[ACCORDION-END]


[ACCORDION-BEGIN [Step 3: ](Configure access to your virtual machine)]

Click on the name of the instance

![Configure VM](vm.png)

Select and copy (`CTRL+C`) the external IP address.

![Configure VM](IP.png)

Click the **Notepad** icon on the task bar and replace any existing IP address with the one you have copied.

![Configure VM](host.png)

The IP address should be followed by a space and `hxehost`

> Delete or comment out other entries with `hxehost`

Save the file.

Read the following text to answer the question below.

> ### **SAP HANA and tutorials for free**
> SAP HANA, express edition is a streamlined version of SAP HANA. The license is provided for free, even for productive use, up to 32 GB of RAM.
>&nbsp;
>In other words, you could SAP HANA, express edition for advanced analytics, as a development platform to later deploy on SAP Cloud Platform, for training or trying the latest SAP HANA features for free.
>&nbsp;
>You can run SAP HANA, express edition on any hardware, like a laptop or on Google Cloud. You may also be eligible for free initial credits that will allow you to use the infrastructure also free of charge.
>&nbsp;
>Find out more about how to deploy SAP HANA, express edition and access hundreds of free, step-by-step tutorials for developers at `developers.sap.com`

[VALIDATE_1]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 4: ](Connect to SAP Web IDE for SAP HANA)]

You will now connect to SAP Web IDE for SAP HANA. This is the editor in which you can create cloud-native, data-driven applications based on micro-services architecture.

Open a new **incognito Google Chrome window**.

![Incognito Chrome](incognito.png)

Enter the following URL:

```text
https://hxehost:39030
```

> ### **Congratulations!**
>You have successfully deployed and configured an SAP HANA, express edition virtual machine on Google Cloud.
>&nbsp;
>

You can continue with the next tutorial using your newly-created instance.

![Incognito Chrome](running.png)

Click on `webide` to complete the validation below. Paste the URL into the box below to complete the validation.

> If you get a `503 Service Unavailable` message, wait a couple of more seconds while the applications finish starting.

[VALIDATE_2]
[ACCORDION-END]
