This script mainly used for create new launch config aur copy from current with update userdata aur any other values. 
beacuase as of now AWS not provide Funcility to update launch config.

first you need to configure aws cli 

1. Update autoscaling groups name in asg_var(in array)
2. run genrate_userdata_from_lc (bash script)that script will genrate userdata of all launch config userdata in userdata_files directory which associate with provided autoscaling groups. then update userdata as required
3. then run create-lc-and-update-asg (bash script) that will create new launch config with updated userdata and update newly launch config to Autoscaling group.

Note:- if you are creating multiple launch config in a day please update launch config name accordingly. because newly created launch cofngi by date in name.
You can update DATE variable like below

#DATE=`date +%Y%m%d-1`
#DATE=`date +%Y%m%d-2`
