# lab9

Python Exceptions and Error Handling

from netmiko import connectHandler

from getpass impot getpass


user = input('Please enter your username: ')

secret = getpass('please enter your password: ')


ciscoDevice = {

        'device_type': 'cisco_ios',
        'host': '192.168.1.9',
        'username': user,
        'password': secret
}

try:
    continue = connectHandler(**ciscoDevice)
except (NetmikotimeoutException):
    print ('The following device timed out: ' + ciscoDevice['host'])
    
print('the script has completed')
