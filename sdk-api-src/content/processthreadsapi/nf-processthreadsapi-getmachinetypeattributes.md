---
UID: NF:processthreadsapi.GetMachineTypeAttributes
tech.root: processthreadsapi
title: GetMachineTypeAttributes
ms.date: 09/28/2021
targetos: Windows
description: Queries if the specified architecture is supported on the current system, either natively or by any form of compatibility or emulation layer. 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - Kernel32.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
api_name:
 - GetMachineTypeAttributes
f1_keywords:
 - GetMachineTypeAttributes
 - processthreadsapi/GetMachineTypeAttributes
dev_langs:
 - c++
---

## -description

Queries if the specified architecture is supported on the current system, either natively or by any form of compatibility or emulation layer.

## -parameters

### -param Machine

An IMAGE_FILE_MACHINE_* value corresponding to the architecture of code to be tested for supportability. See the list of architecture values in [Image File Machine Constants](/windows/win32/sysinfo/image-file-machine-constants).

### -param MachineTypeAttributes

Output parameter receives a pointer to a value from the [MACHINE_ATTRIBUTES](ne-processthreadsapi-machine_attributes.md) enumeration indicating if the specified code architecture can run in user mode, kernel mode, and/or under WOW64 on the host operating system.

## -returns

If the function fails, the return value is a nonzero HRESULT value. If the function succeeds, the return value is zero.

## -remarks

## -see-also
