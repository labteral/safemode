# safemode
Replace the Python process with a shell when starting up if a key is pressed during a grace period.

## Install
```bash
pip install safemode
```

## Usage
Just import the library in the first line of your Python script. The grace period can be configured through the `SAFEMODE_GRACE_PERIOD` environment variable. The default value is 5 seconds.

main.py
```python
import stopover
print('Hello World')
```

Safe mode:
```sh
$ python main.py
[safemode] To start a shell, press any key before 5 seconds...
$
```

Normal execution:
```sh
$ python main.py
[safemode] To start a shell, press any key before 5 seconds...
[safemode] Starting up normally...
Hello World
```
