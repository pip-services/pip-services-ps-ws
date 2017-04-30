# <img src="https://github.com/pip-services/pip-services/raw/master/design/Logo.png" alt="Pip.Services Logo" style="max-width:30%"> <br/> Workspace for Pip.Services in Powershell

This is a workspace for [Pip.Services](https://github.com/pip-services/pip-services) frameworks implemented in Powershell.
It enables build, test, and release across the following projects:

- **pip-services-devenv** - dockerized infrastructure services for development and testing
- **pip-services-facade-ps** - Client facade components
- **pip-facade-infrastructure-ps** - Integration with infrastructure client facade
- **pip-facade-users-ps** - Integration with users management client facade
- **pip-facade-content-ps** - Integration with content management client facade
- **pip-facade-support-ps** - Integration with product support client facade

## Installation

- Install **pip-tasks-ps**, **pip-tasks-common-ps** Powershell modules, 
add them to **PSModulePath** and import into Powershell

- Clone this workspace to local disk
```bash
> git clone https://github.com/pip-services/pip-services-ps-ws.git
```

- Got to the workspace folder and clone component repositories
```bash
> piptask clone -workspace
```

## Usage

- Setting default workspace
```bash
> pipuse <Path to this workspace>
```

- Start and stop infrastructure services
```bash
> piptask start -component pip-services-devenv
> piptask stop -component pip-services-devenv
```

- Test all components
``` bash
> piptask test -all
```

- Check out changes from remote repository
```bash
> piptask pull -all
```

- Check in changes to remote repository
```bash
> piptask push -m <Changes comment> -all
```

## Acknowledgements

The Powershell version of Pip.Services is created and maintained by **Sergey Seroukhov**
