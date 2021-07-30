# Hideproc

A kernel module that hide specific process.

## Build

Confirm your kernel version.

```shell
uname -r
```

### Kernel v5.7+

```shell
cd kernel57up
make
sudo insmod hideproc
```

### Old kernel

```shell
cd oldkernel
make
sudo insmod hideproc
```

## Run

If you want to hide the process with pid 1322 with its parent process.

```shell
echo "add 1322" | sudo tee /dev/hideproc
```

Unhide it.

```shell
echo "del 1322" | sudo tee /dev/hideproc
```

List current hiding pids.

```shell
sudo cat /dev/hideproc
```

## More infomations

[My hackmd link](https://hackmd.io/@Zeng/hideproc)
