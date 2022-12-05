---
UID: NE:processthreadsapi._THREAD_INFORMATION_CLASS
title: THREAD_INFORMATION_CLASS (processthreadsapi.h)
description: The THREAD_INFORMATION_CLASS enumeration (processthreadsapi.h) specifies the collection of supported thread types.
tech.root: processthreadsapi
ms.date: 10/31/2022
helpviewer_keywords: ["THREAD_INFORMATION_CLASS"]
ms.keywords: 'THREAD_INFORMATION_CLASS'
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: THREAD_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _THREAD_INFORMATION_CLASS
 - processthreadsapi/_THREAD_INFORMATION_CLASS
 - THREAD_INFORMATION_CLASS
 - processthreadsapi/THREAD_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - THREAD_INFORMATION_CLASS
---

# THREAD_INFORMATION_CLASS enumeration

## -description

Specifies the collection of supported thread types.

## -enum-fields

### -field ThreadMemoryPriority

Lower the memory priority of threads that perform background operations or access files and data that are not expected to be accessed frequently.

### -field ThreadAbsoluteCpuPriority

CPU priority.

### -field ThreadDynamicCodePolicy

Generate dynamic code or modify executable code.

### -field ThreadPowerThrottling

Throttle the target process activity for power management.

### -field ThreadInformationClassMax

## -remarks

## -see-also

[UnmapViewOfFile2 function](../memoryapi/nf-memoryapi-unmapviewoffile2.md), [UnmapViewOfFileEx function](../memoryapi/nf-memoryapi-unmapviewoffileex.md), [GetThreadInformation function](nf-processthreadsapi-getthreadinformation.md), [SetThreadInformation function](nf-processthreadsapi-setthreadinformation.md), [PROCESS_MITIGATION_DYNAMIC_CODE_POLICY structure](../winnt/ns-winnt-process_mitigation_dynamic_code_policy.md), 