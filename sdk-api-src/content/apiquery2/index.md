---
UID: NA:apiquery2
title: Apiquery2.h header
description: The apiquery2.h header declares functions that query the API set schema composed on the running device.
ms.assetid: 2c1cf2bf-a7a5-3d90-a712-935f2e90a02c
ms.date: 09/01/2026
ms.keywords: 
ms.topic: overview
ms.update-cycle: 1095-days
tech.root: winprog
f1_keywords:
 - apiquery2
 - apiquery2/apiquery2
---

# Apiquery2.h header


## -description

Declares functions that query the [API set](/windows/win32/apiindex/windows-apisets) schema composed on the running device.

Win32 APIs in the core OS are organized into functional contracts called API sets. The Windows loader resolves an API set name to the module that implements it, and that mapping varies by Windows edition, device, and enabled features. The functions in this header report what the mapping on the current device says:

- [IsApiSetImplemented](./nf-apiquery2-isapisetimplemented.md) reports whether an API set is available.
- [GetApiSetModuleBaseName](./nf-apiquery2-getapisetmodulebasename.md) returns the base name recorded in the schema for the module that implements it.

To gate a call to an API that isn't available on every Windows device, see [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability).

## -remarks

### Supported environment

The declarations in this header are available to the user-mode Desktop and System API partitions.

### What these functions report

Both functions read the composed API set schema. Neither one probes the file system, opens the implementing module, or checks that a particular function is exported from it.

A result is contract- or group-granular, not function-granular. Use it to decide whether to enter an optional code path, and then handle module-loading errors, missing exports, and the API's own documented failure results as usual.

### The two functions have different availability models

**IsApiSetImplemented** is reachable through the OneCore umbrella libraries, and the compatibility implementation supplied by *OneCore.lib* lets a binary that links it also run on versions of Windows that predate the underlying query support.

**GetApiSetModuleBaseName** is carried by a later contract version, `api-ms-win-core-apiquery-l2-1-1`. Treat it as an advanced API: gate it with **IsApiSetImplemented**, then bind to it with **LoadLibrary** and **GetProcAddress** rather than through an import library, so that a binary that also runs on systems that predate the function still loads.

Linking, dynamic binding, downlevel behavior, and buffer rules are covered on the individual function pages.

## -see-also

* [Windows API sets](/windows/win32/apiindex/windows-apisets)
* [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability)
