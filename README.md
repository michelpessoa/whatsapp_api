# WhatsApp Group API on Selenium
Easy to use API on selenium to have control of a WhatsApp group using the web browser. 

### Implemented features
- Get all contacts from a selected group
```
In [1]: from whatsapp_api import WhatsApp
In [2]: wp = WhatsApp()
Loading...
Please scan the QR Code and enter in the group
In [3]: wp.get_group_numbers()
```
- Write and/or send messages
```
In [1]: from whatsapp_api import WhatsApp
In [2]: wp = WhatsApp()
Loading...
Please scan the QR Code and enter in the group
In [3]: wp.send_message('This message is going to be sent')
In [4]: wp.write_message('This message is going to be written but not sent')
```
- Search for a contact given a keyword (phone number or name)
```
In [1]: from whatsapp_api import WhatsApp
In [2]: wp = WhatsApp()
Loading...
Please scan the QR Code and enter in the group
In [3]: wp.search_contact('+55000000000')
```
- Phone number parser for performing set operations
```
    >>> group_numbers = wp.get_group_numbers()
    >>> group_numbers = wp.parser(group_numbers[:-1]) # Remove last contact which is not a number ('You')
    >>> all_numbers = [...]
    >>> all_numbers = wp.parser(all_numbers)
    >>> not_joined = all_numbers - group_numbers
```


### Possible future features
- ?

### Requirements
- Selenium: `pip install selenium`
- ChromeDriver: http://chromedriver.chromium.org/
    - After downloading chromedriver, make sure to add in a folder accessible from the PATH

### LICENCE
MIT
