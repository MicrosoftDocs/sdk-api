---
UID: NS:processthreadsapi._PROCESS_MACHINE_INFORMATION
tech.root: security
title: PROCESS_MACHINE_INFORMATION
ms.date: 09/28/2021
targetos: Windows
description: Specifies the architecture of a process and if that architecture of code can run in user mode, kernel mode, and/or under WoW64 on the host operating system.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: processthreadsapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: PROCESS_MACHINE_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - _PROCESS_MACHINE_INFORMATION
 - PROCESS_MACHINE_INFORMATION
f1_keywords:
 - _PROCESS_MACHINE_INFORMATION
 - processthreadsapi/_PROCESS_MACHINE_INFORMATION
 - PROCESS_MACHINE_INFORMATION
 - processthreadsapi/PROCESS_MACHINE_INFORMATION
dev_langs:
 - c++
---

# PROCESS_MACHINE_INFORMATION structure

## -description

Specifies the architecture of a process and if that architecture of code can run in user mode, kernel mode, and/or under WoW64 on the host operating system.

## -struct-fields

### -field ProcessMachine

An IMAGE_FILE_MACHINE_* value indicating the architecture of the associated process. See the list of architecture values in [Image File Machine Constants](/windows/win32/sysinfo/image-file-machine-constants).

### -field Res0

Reserved.

### -field MachineAttributes

A value from the [MACHINE_ATTRIBUTES](ne-processthreadsapi-machine_attributes.md) enumeration indicating if the process's architecture can run in user mode, kernel mode, and/or under WOW64 on the host operating system.

## -remarks

## -see-also

[PROCESS_INFORMATION_CLASS](ne-processthreadsapi-process_information_class.md)
