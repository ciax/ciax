- 👋 Hi, I’m @ciax
- 👀 I’m interested in control program and IoT.
- 🌱 I’m currently learning ruby,bash and Javascript.
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
# What is CIAX?
 CIAX is an abbreviation for CASSEGRAIN INSTRUMENT AUTOMATED EXCHANGER, which is a system to automatically exchange instruments on the Japanese government-owned Subaru Telescope in Hawaii. Astronomical instruments, which are the main body of the camera of the Subaru Telescope, are detachable, and multiple instruments need to be replaced whenever desired. CIAX is a system of automated guided vehicles and standby hangars to perform this exchange. The CIAX system is an application of factory automation, but it differs from the factory system in that it requires very heavy instruments to be mounted in a limited space with precise positioning.
# What's here?
 Here is the code that controls the CIAX system. This is the part that communicates with various devices through the network and operates them according to a sequence. It is also known as a distributed control system. As development progressed, it evolved from something specific to CIAX to something more general. It is currently being used to control the robot of MOIRCS, one of Subaru's observation instruments. There are also tools available to improve the development environment on LINUX. The contents of each repository are as follows.
 ```mermaid
  graph TD;
   ciax-xml;
   utils -->cfg.*;
   ```
 ## ciax-xml
  It consists of device and sequence configuration files and their accompanying scripts. For more information, please refer to the repository wiki.
 ## utils
  This is a collection of BASH scripts to improve the development environment. Various management tools are also included. It is not necessarily required for CIAX-XML, but it is useful to have.
 ## cfg.*
 These are managed in the "utils" configuration file and are separated by disclosure range. For private information, please prepare your own repository with a name such as "cfg.priv".
 ## etc.
  - drivers
   The old version of CIAX codes written in Perl. 
# How to install?
 It is recommended that you install "utils". If you already have a familiar environment, CIAX-XML will work without it.
 > Note: The software is designed to set up the environment in a way that minimizes the need to modify existing configuration files. All executable scripts are linked under "~/bin" in the home directory, and additions to the PATH environment variable are kept to a minimum. If you want to make a new script executable, you must first "register" the file.
 ## Shell Utilities (utils)
  You download config file first. It includes a setup script file to be invoked.
  ```
  $ git clone https://github.com/ciax/cfg.naoj.git
  $ ~/cfg.naoj/setup
  ```
  This script will download a more public configuration repository and invoke "setup" in it. This is a chain of events that will eventually install "utils" for you. If you can use "sudo" as an administrator, the necessary applications will be automatically recognized and installed.
 ## CIAX-XML (Distributred Control System)
  Just do as follows and run "setup".
  ```
  $ git clone https://github.com/ciax/ciax-xml.git
  $ ~/ciax-xml/utils/setup-ciax.sh
  ```
# How to Setup/Use?
 See each repository's wiki for configuration and usage.
<!---
ciax/ciax is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
