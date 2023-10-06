# A Kernel Seedling
The proc_count kernel module creates a file /proc/count that shows the current number of running processes.

## Building
```shell
make
```

## Running
```shell
sudo insmod proc_count.ko
cat /proc/count
```
This will print an integer - the current number of running processes - followed by a newline.

## Cleaning Up
```shell
sudo rmmod proc_count
make clean
```

## Testing
```python
python -m unittest
```
The unit tests should succeed within reasonable time, and will output a message indicating that all 3 tests succeeded, as well as the time they took to execute.

This module was tested on Linux 5.14.8.
