# cwe

Send a single event to CloudWatch Events on the command line.

This tool is much easier to use on the command line than the AWS CLI, plus it is contained within a single statically-linked binary so there's no dependencies to manage.  Simply download and run.

## Requirements

* AWS access key and secret key (discoverable by env vars or via the EC2/ECS metadata service)
* Permission to send CloudWatch events (i.e. `events:PutEvents`)

## Usage

Send a single event:

```bash
cwe --source "com.example.app" --resources i-103932,i-10393 --type "A test event" --detail "\"Key\": \"Value\""
```

or use the short-form flags:

```bash
cwe -s "com.example.app" -r i-103932,i-10393 -t "A test event" -d "\"Key\": \"Value\""
```
