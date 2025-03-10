
# Installing Docker and AlmaLinux9 on macOS (Apple M2 Chip)


This *user friendly* spe-by-step guideline will help you throughout the procedure required to install **Docker** on a Mac with **Apple M2 chip**.

---

## Docker 

### Step 1: Check System Requirements
Before starting to proceed, make sure your Mac meets the following requirements:

 - **At least 4GB of RAM** (Recommended: 8GB or more)
 - **At least 10GB of free disk space**
 - **An active internet connection**

To check whether you have enough RAM and disk space, click on the Apple logo (top-left corner) → "About This Mac" -> "More info".

### Step 2: Download and Install Docker Desktop App
1. Open your web browser and go to the official [Docker website](https://www.docker.com/products/docker-desktop/).
2. Click the **"Download for Mac"** button. Make sure to select the version for **Apple Silicon (M1/M2)**.
3. Once the dowload is over, open the file (go to *Downloads* folder or you ca find it straight on in the *Downloads* button of your browser
4.  To complete the installation, follow the instruction visualised in the pop-up window **drag and drop the Docker icon into the Applications folder**. 
5. You may want to check if the installation procedure was successful: open the Terminal and run " docker --version "

### Step 3: Account Docker
*Docker Desktop app may ask for *administrator permissions.*

 1. Click on the **Docker whale icon 🐳** and allow for local network connection
 2. Accept **Docker Subscription Service Agreement** terms
 3. Create your own account and verify your e-mail address. You will be redirected to the desktop app automatically after this procedure.

Congratulations! Docker is now installed and running on your Mac, you're ready go!

---

## AlmaLinux 9
Now that you have successfully installed Docker Desktop App, you're good to go with the next step: installing AlmaLinux9 distribution. 
Here's a simple guideline: Click on the **Docker whale icon** to open the app, go to **Dashboard** to use its interface and follow the instructions below.

### Download the AlmaLinux 9 Image
1. In the **Docker Dashboard**, click on the **"Images"** tab.
2. In the search bar, type `almalinux:9` and press Enter.
3. Click **Pull** to download the latest AlmaLinux 9 Image.

Alternatively, click on the Docker **>_Terminal** button (bottom right corner) to open up a Terminal window directly on the Docker App, type " docker pull almalinux:9 " and press *Enter*.

### Create and Run an AlmaLinux 9 Container
1. Once the image has been downloaded, go to the **Containers** tab.
2. Click **"Create Container"**
3. Once in the set-up window, you can choose to name your new container as you please (e.g., `my-almalinux`). The **Image** field should now show `almalinux:9` and the **Name** field correspond to your choice
4. Click **Run** to start the container.
5. Click on the 3 dots in the **Action** field and click on *Open in Terminal* to start typing instructions

Alternatively, continue on the Docker **>_Terminal**,  type `docker run -it --mycontainername AL9-container almalinux:9 /bin/bash` and press *Enter*.

You now find your `my-almalinux` container running and be able to proceed in the Terminal window. Further check: to test that everything is working, type: `cat /etc/os-release` and you should see all the details about AlmaLinux 9.

