## Purpose

The **µOS++ IIIe** _(micro oh ɛs plus plus third edition)_ project is the third iteration of µOS++, a POSIX-like, portable, open source, royalty-free, multi-tasking real-time operating system intended for 32/64-bits embedded applications, written in C++. 

**CMSIS++** is a proposal for a future CMSIS, written in C++, and is the core component of µOS++ IIIe, defining the system APIs. These APIs are documented in the [CMSIS++ reference](http://micro-os-plus.github.io/reference/cmsis-plus/).

**POSIX++** is another point of view of the project; with most system APIs using the POSIX semantics, but being written in C++, the **µOS++ IIIe** APIs can also be seen as a C++ version of POSIX, thus the name **POSIX++**.

## Status

The µOS++ project is fully functional for Cortex-M devices and also runs on synthetic POSIX platforms (like macOS and GNU/Linux).

## Related projects

The current µOS++ code tries to be as portable as possible.

Specific implementations are available from separate projects:

- the Cortex-M port of the scheduler is packed as [µOS++ IIIe Cortex-M xPack](https://github.com/micro-os-plus/micro-os-plus-iii-cortexm)
- the synthetic POSIX port of the scheduler is packed as [POSIX arch xPack](https://github.com/micro-os-plus/posix-arch)

## Build Configuration

To include µOS++ in a project, in addition to one of the port specific project, consider the following details:

### Include folders

- `include` 
 
### Source folders

- `src` 

### Symbols

See [CMSIS++ Application Config](http://micro-os-plus.github.io/reference/cmsis-plus/group__cmsis-plus-app-config.html).

## Documentation

* [µOS++ IIIe](http://micro-os-plus.github.io)
* [CMSIS++ reference](http://micro-os-plus.github.io/reference/cmsis-plus/)
* the original ARM CMSIS documentation is available form 
[keil.com](http://www.keil.com/pack/doc/CMSIS/General/html/index.html)

## Demo projects

Examples on how to structure projects using µOS++, including integration with CubeMX for STM devices, can be found in the separate [GitHub project](https://github.com/micro-os-plus/eclipse-demo-projects).

## Tests

* tests/rtos - simple test to exercise the CMSIS++ RTOS C++ API, the C API and the ISO C++ API
* tests/mutex-stress - a stress test with 10 threads fighting for a mutex
* tests/sema-stress - a stress test posting to a semaphore from a high frequency interrupt.
* tests/gcc - compile test with host GCC compiler

The ARM CMSIS RTOS validator is available from a [separate project](https://github.com/xpacks/arm-cmsis-rtos-validator).

To run these tests, several Eclipse projects are available in a separate [GitHub project](https://github.com/micro-os-plus/eclipse-test-projects).

## License

µOS++ is provided free of charge under the terms of the [MIT License](https://opensource.org/licenses/MIT).


