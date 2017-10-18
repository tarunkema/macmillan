# macmillan
import boto3        # this package is for AWS SDK kit for python#
import logging      # importing logging package for python#
import time         # importing time to sechdule to run it at specific time #
import argparse
import InfluxDBClient
Import os

delay=60*5  ### for ever 5 minutes delay###
close_time=time.time()+delay
while True:
aws_access_key = 'PSRHGOIH8567484OPSAJEPHI'
aws_secret_key = 'AOHFIGEJ79WE797E7WE'
region = 'us-east-1'
logger = logging.getLogger()
logger.setLevel(logging.INFO)
ec2 = boto3.resource('ec2')
def lambda_handler(event, context):
    
    filters = [{
            'Name': 'tag:Auto-on',
            'Values': ['True']
        },
        {
            'Name': 'instance-state-name', 
            'Values': ['running']
        }
    ]
    
        instances = ec2.instances.filter(Filters=filters)
    RunningInstances = [instance.id for instance in instances]
    
        print RunningInstances
client = InfluxDBClient(mcmillan.systems.net, 8086 , root , root$$$666, Mcmillan-learning)
client.create_database(Mcmillan-learning)
client.write_points(Running Instances)

if time.time()>close_time
         break
