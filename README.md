# Use the latest 2.1 version of CircleCI pipeline processing engine, see
https://circleci.com/docs/2.0/configuration-reference/ version: 2.1  

# Use a package of configuration called an orb, see https://circleci.com/docs/2.0/orb-intro/ 
orbs:   
  # Declare a dependency on the welcome-orb   
    welcome: circleci/welcome-orb@0.3.1  

# Orchestrate or schedule a set of jobs, see https://circleci.com/docs/2.0/workflows/ 
workflows:   
  # Name the workflow "Welcome"   
  Welcome:     
    # Run the welcome/run job in its own container     
    jobs:       
    - welcome/run
