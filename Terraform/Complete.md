1. Variables
2. Variable types ( string, number, bool, List)
3. Functions (join, upper, lower, lookup)
4. Map Variable
5. TFVARs Files
6. Read Variables from your system(export TF_VAR_username=tauqir)
7. Terraform Core and Plugin
8. .tfstate file and lock .tfstate file
9. destroy command
10. Terraform validate
11. Terraform refresh (when you change some thing manually by console and want to update that in terraform file also)
12. Terraform Output
13. Terraform console ( to see variables values)
14. Terraform fmt (correct format of data in files )
15. Dynamic Block 
16. Terraform Taint (When we want to recreate a new specific resource may be security group or any thing)
17. File Provisioner (file, local-exec, remote-exec)--------> to send file from local to remote
18. Terraform workspace (when need to setup multiple env)
19. Terraform datasource (AMI id can be changed in aws that's why we use it )
20.  Terraform Modules
21. Terraform Backends 



### Terraform Workspaces

We can use one terraform file for both enviroments. We can use this variable to achieve this ${terraform.workspace}-instancename


![[Pasted image 20250514202115.png]]



![[Pasted image 20250514203316.png]]


Question: How it manage tfstate file may be anything overrides.

If we have 2 workspaces name with dev and test each workspace have different tfstate file
.terraform/
└── terraform.tfstate.d/
    ├── dev/
    │   └── terraform.tfstate
    └── test/
        └── terraform.tfstate


### Terraform Data Sources



/home/totalscope/server_sh_files

/var/www/sites

/home/devops/.pm2

pm2 logs tscope-prod-api-server --lines 100

pm2 logs 7

ps aux | grep tscope_prod_api_server_health.sh

tail -f /root/.pm2/logs/tscope-dev-api-server-out.log

curl -s https://totalscope2024.com/api/health | jq .

grep -i "restart" tscope_prod_api_server_health.log

awk '/Restarting PM2 process/ {print NR}' tscope_prod_api_server_health.log | while read -r line; do

grep -i "restart" tscope_prod_api_server_health.log
