# Minimal Reproducible Example

To reproduce:

```console
$ pwd
/home/noah/setuptools-bug-demo
$ python3 -m venv env
$ source env/bin/activate
$ pip install --upgrade pip setuptools wheel
$ pip install -e bugexample
$ pip install -e workingexample
$ python
```
```python3
>>> import bugexample
>>> import working
>>> bugexample.obj
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: module 'bugexample' has no attribute 'obj'
>>> working.obj
'Yay! :D'
```
```console
cd ~
python
```
```python3
>>> import bugexample
>>> import working
>>> bugexample.obj
'Oh no!'
>>> working.obj
'Yay! :D'
```
