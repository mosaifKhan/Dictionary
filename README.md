# Dictionary
I am creating dictionary using list in Python.

>>> data = {1:'Mosaif', 2:'Saif', 4:'Kaif'}
>>> data
{1: 'Mosaif', 2: 'Saif', 4: 'Kaif'}

>>> data[1]
'Mosaif'
>>> data [4]
'Kaif'
>>> data [2]
'Saif'
>>> data[3]                              //# Here key (3) is not specified in the dictionary so that it produce error function.
Traceback (most recent call last):
  File "<pyshell#6>", line 1, in <module>
    data[3]
KeyError: 3
  
  >>> data.get(1)
'Mosaif'

>>> data.get (2)
'Saif'

>>> data.get(4)
'Kaif'

>>> data.get(3)                           
>>>                                      //# Here key (3) is not specified in the dictionary but niether producing error nor anything else (Only None). So we can add the value 
                                             (Not Found/Not Available) by user to confirm the given key is not in the dictionary. 
>>> print (data.get(3))
None
>>> print (data.get(3,'Not Found'))
Not Found

# Now i am going to merge two list into a dictionary so that i'll use a special function 'zip'.

>>> key = ['Mosaif', 'Harsh', 'Navin']
>>> values = ['Python', 'Java', 'JS']

>>> data = dict(zip(key,values))
>>> data
{'Mosaif': 'Python', 'Harsh': 'Java', 'Navin': 'JS'}

>>> data ['Mosaif']
'Python'
>>> data ['Harsh']
'Java'
>>> data['Navin']
'JS'

# Now i am going to add some fey in dictionary

>>> data ['Monika'] = 'SQL'                                            //# Adding key
>>> data
{'Mosaif': 'Python', 'Harsh': 'Java', 'Navin': 'JS', 'Monika': 'SQL'}

>>> data ['Monika']
'SQL'

>>> del data ['Navin']                                                 //# Deleting key
>>> data
{'Mosaif': 'Python', 'Harsh': 'Java', 'Monika': 'SQL'}


# Now i am going to create dictionary into dictionary using list.

>>> mk = {'JS': 'Atom', 'CS': 'VS', 'Python': ['Pycharm', 'Sublime'], 'Java': {'JSE': 'Netbeans', 'JEE': 'Eclipse'}}
>>> mk
{'JS': 'Atom', 'CS': 'VS', 'Python': ['Pycharm', 'Sublime'], 'Java': {'JSE': 'Netbeans', 'JEE': 'Eclipse'}}

>>> mk ['Python']
['Pycharm', 'Sublime']

>>> mk['Python'][1]
'Sublime'

>>> mk ['Java']
{'JSE': 'Netbeans', 'JEE': 'Eclipse'}

>>> mk ['Java']['JEE']
'Eclipse'

>>> mk ['Java']['JSE']
'Netbeans'
