# Jenkins and Github Integration using PollSCM, Job Chaining and Remote Triggers, git hooks.

## Integrating Jenkins with local git hooks and deploying the 
## source code on docker containers using PollSCM triggers.

Three jobs are needed for simulating this project.

### 1. job1  
For deploying testing environment on the top of docker using git hooks(post-commit)
---------------------- post-commit ------------------------------------
  #!/bin/bash
  echo "First <git fetch> and then Post Commit Tasks are started"                                                     
  git fetch                                                                                                              
  git push                                                                                                                
  echo "git push is done to the current Remote Branch"                                                                   
  #echo "remote Build Trigger using jenkins URL"                                                                          
  #curl --user "<user>:<password>" <Remote Build Trigger URL> 
-----------------------------------------------------------------------
![Job1 configuration](/images/job1i1.png)

