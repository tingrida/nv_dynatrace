## STATE

raw working version. No sanity chdecks!

# USE CASES

## ANSIBLE

### PREREQUISITES
- **inventory.ini**: put all hosts whit dynatrace one agent under group dynatrace to start/stop  and reassing oneagents with playbooks

### PLAYBOOKS
- **get_ec2_facts.yaml**:  playbook to get ec2 facts for instances
- **start_ec2_instances.yaml**: starts ec2 instances with Name Dynatrace_Manageds, starts dynatrace and oa on them, starts oa on servers in group dynatrace and sets oa to report to right node(s)
- **stop_ec2_instances.yaml**: stops oa on nodes in group dynatrace, stops oa and dynatrace on ec2 instances with Name tag Dynatrace_Manages, stops ec2 instances 