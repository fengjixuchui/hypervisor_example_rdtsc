# Bareflank Hypervisor RDTSC Example

## Description

This example demonstrates how to extend the Bareflank hypervisor to
emulate the RDTSC instruction. For more information on how Bareflank
extensions work, please see the following:

[API Documentation](http://bareflank.github.io/hypervisor/html/)

## Compilation / Usage

To setup our extension, run the following (assuming Linux):

```
git clone https://github.com/Bareflank/hypervisor
git clone https://github.com/Bareflank/hypervisor_example_rdtsc.git
mkdir build; cd build
cmake ../hypervisor -DDEFAULT_VMM=example_vmm -DEXTENSION=../hypervisor_example_rdtsc
make -j<# cores + 1>
```

To test out our extended version of Bareflank, run the following commands:

```
make driver_quick
make quick
```

to get status information, use the following:

```
make status
make dump
```

to reverse this:

```
make unload
make driver_unload
```
