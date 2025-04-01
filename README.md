
# GBApp

## Overview

**GBApp** GBApp is an intuitive web application for Growth Balance Analysis (GBA) of self-replicating cell models. Built with R/Shiny, it features a user-friendly, spreadsheet-style interface that enables researchers to model cellular resource allocation under nonlinear kinetic constraints. GBApp streamlines model construction by integrating enzyme kinetics and parameter data from the BRENDA database, providing interactive matrix-based model setup, and generating dynamic visualizations of metabolic pathways. By lowering computational barriers, GBApp makes nonlinear cellular modeling more accessible to the broader scientific community.

🔗 **Try GBApp online:** [GBApp Web Application](https://gba.ccb.cs.hhu.de/) 

This repository contains all the necessary source code and Docker configuration files for building and running GBApp locally or on a server.

1. **Source Code** for the GBApp Shiny application (in the `GBApp` directory)  
2. **Dockerfile** for building and running the GBApp container locally or on a server

---

## Quick Start: Running GBApp via Docker

These instructions let you build and run the GBApp Docker container on your local machine.

1. **Install Docker**  
   - [Docker Desktop](https://www.docker.com/products/docker-desktop) for macOS, Windows, or Linux.

2. **Clone or Download this Repository**

   ```bash
   git clone https://github.com/Sijr73/GBApp.git
   cd GBApp

3. **Build the Docker Image**

   For M1/M2 (ARM-based) Macs or any ARM-based system, specify the AMD64 platform to ensure compatibility:
   ```bash
   docker build --platform=linux/amd64 -t gba-app .
   ```

4. **Run the Docker Container**

   ```bash
   
   docker run -d -p 3838:3838 --name gba-app gba-app
   ```
   `-d`: run the container in detached mode

   `-p 3838:3838`: map port 3838 in the container to port 3838 on your machine

5. **Open GBApp**

   - Go to http://localhost:3838 in your web browser.
   - You should see the GBApp home page.

