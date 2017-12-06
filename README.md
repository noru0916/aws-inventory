# Inventory

AWS Inventory tool. Useful to get summarized information on an client's AWS account for a Cloud Assessment report.  The tool is produces tab separated output that can be pasted into a spreadsheet and then copied to a Cloud Assessment report.

## Usage

```sh
exe/inventory cfn
exe/inventory ec2
exe/inventory vpc
exe/inventory sg
exe/inventory rds
exe/inventory route53
exe/inventory acm
exe/inventory elb
exe/inventory eb
exe/inventory ecs
```

## Example

What the output looks like:

```sh
$ exe/inventory ec2
Name  Instance Id Instance Type Security Groups
name1 i-123 t2.micro  sg1,sg2
name2  i-456 c3.2xlarge  s1
```

You want to pipe this into a tool like pbcopy so that tabs, not spaces are copied into your buffer.  Example:

```sh
$ exe/inventory ec2 | pbcopy
```
