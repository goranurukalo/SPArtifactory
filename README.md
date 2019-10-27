# SPArtifactory
> Manage SPA production builds and makes shipping easier

<br/>
This is going to be tool that will help you with frontend deployment.
<br/>
It will be similar to other repository managing tools (we need to create simple integration with other tools).
<br/>
This project will have 3 main components right now:
  - repository
  - agent
  - ui

<br/>
<br/>
Repository: place where we can push new version of application to
<br/>
Agent: tool that will execute actions for us [fetch, update, rollback, etc..]
<br/>
UI: this is going to be part of repository, way to configur and monitor our packages
<br/>


# Flow
> example of create-react-app deployment

1. # ssh to server A
1. npm run build
1. *agent* push # configuration in separate file
1. # ssh to server B
1. *agent* update *app-name* # agent needs configuration to repository server

<br/>

# WHY?
Sometimes you can have bug in your SPA, you wish to rollback app to previus version
<br/>
Or you would like to have same app on multiple servers.
<br/>
Idea is to have similar tool as `npm` but for SPA build artifact.
