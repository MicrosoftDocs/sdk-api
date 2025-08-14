---
UID: NE:processthreadsapi._MACHINE_ATTRIBUTES
tech.root: processthreadsapi
title: MACHINE_ATTRIBUTES (processthreadsapi.h)
ms.date: 09/28/2021
targetos: Windows
description: Specifies the ways in which an architecture of code can run on a host operating system.  More than one bit may be set.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: processthreadsapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - _MACHINE_ATTRIBUTES
 - MACHINE_ATTRIBUTES
f1_keywords:
 - _MACHINE_ATTRIBUTES
 - processthreadsapi/_MACHINE_ATTRIBUTES
 - MACHINE_ATTRIBUTES
 - processthreadsapi/MACHINE_ATTRIBUTES
dev_langs:
 - c++
---

# MACHINE_ATTRIBUTES enumeration

## -description

Specifies the ways in which an architecture of code can run on a host operating system. More than one bit may be set.

## -enum-fields

### -field UserEnabled : 0x00000001

The specified architecture of code can run in user mode.

### -field KernelEnabled : 0x00000002

The specified architecture of code can run in kernel mode.

### -field Wow64Container : 0x00000004

The specified architecture of code runs by relying on WOW64's namespace [File System Redirector](/windows/win32/winprog64/file-system-redirector) and  [Registry Redirector](/windows/win32/winprog64/registry-redirector). This bit will be set, for example, on x86 code running on a host operating system that is x64 or ARM64. When the compatibility layer does not use WOW64 style filesystem and registry namespaces, like x64 on ARM64 which runs on the root namespace of the OS, this bit will be reset.


## -remarks

## -see-also

