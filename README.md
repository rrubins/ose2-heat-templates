=======================================================
OSE-HA - Heat stack to build out OSE 2.x HA Environment
=======================================================
1. Edit the environmnet file 'ose_ha_env.yaml' to reflect your environment
2. As OpenStack admin, execute the following to build 'ose-ha' stack
	# heat stack-create ose-ha -f ose_ha_stack.yaml -e ose_ha_env.yaml
3. Validate the stack
        # heat stack-list
        # heat stack-show ose-ha
        # heat resource-list ose-ha
        # heat event-list ose-ha
4. Perform post-installation tasks
5. To add additional OpenShift nodes, edit the 'ose_node_env.yaml'
   You will need to adjust at least the following parameters:
   node_hostname = node4	
   
	# heat stack-create ose-node4 -f ose_node_stack.yaml -e ose_node_env.yaml

