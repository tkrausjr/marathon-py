# marathon Python Library
Python Library for interacting with Marathon REST API.

## Objective
To provide a simple way to automate common tasks in Marathon

## Prerequisites
A running DCOS cluster with Marathon v 1.xxx and Python 3 installed on the system.


## Installation

Copy the marathon-client.py file to the same directory as the script that will call it or move it into your Python3 Libraries folder

## Example

	### Calling the Library

		import marathon-client


	### Initialize a Marathon Connection Object -

		new_marathon = marathon-client.Marathon(dcos_master,dcos_auth_token)

	### Get All Marathon Apps -

		apps = new_marathon.get_all_apps()


	### Get Marathon App Details -
		marathon_app = '/dev/nginx01'
		app_details = aws_marathon.get_app_details(marathon_app)

	### Scale Marathon App -
		new_marathon.scale_app(marathon_app, instances)

	### Add Marathon Application -
		marathon_app_json_file = '/Users/tkraus/sandbox/marathon/12b-siege.json'
		new_app = new_marathon.add_app(marathon_app_json_file)
