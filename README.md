# retryd
try something and get except, fast to retry, pass this, or others..


### V0.1


`pip3 install retryd`

```python
# use
@try_except_pass(errors=(IndexError,))
@try_redo(times=10, delay=0)
@failed_todo(function, 'I am Message', 'username', 'pasword')
```




```python
def alert(message, module, name, error, username, password, *args, **kwargs):
    print(message)
    print(module, name)
    print(error)
    print(username)
    print(password)
    return True


# @try_except_pass(errors=(IndexError,))
# @try_redo(times=10, delay=0)
@failed_todo(alert, 'I am Message', 'username', 'pasword')
def rai():
    print('I am main')
    raise IndexError('Fuck')

print(r())


# output
I am main
I am Message
__main__ r
Fuck
username
pasword
True
```

```python
@try_except_pass(errors=(IndexError,))
@try_redo(times=10, delay=0)
def rai():
    print('I am main')
    raise IndexError('Fuck')

print(r())

# output
I am main
I am main
I am main
I am main
I am main
I am main
I am main
I am main
I am main
I am main
Fuck
```
