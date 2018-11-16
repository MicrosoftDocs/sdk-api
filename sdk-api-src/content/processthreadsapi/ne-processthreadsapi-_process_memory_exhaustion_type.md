---
UID: NE:processthreadsapi._PROCESS_MEMORY_EXHAUSTION_TYPE
title: "_PROCESS_MEMORY_EXHAUSTION_TYPE"
author: windows-sdk-content
description: Represents the different memory exhaustion types.
old-location: base\process_memory_exhaustion_type.htm
tech.root: ProcThread
ms.assetid: 0A5B6B4D-B2FF-4873-85E0-3CCB3EA3BF91
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PPROCESS_MEMORY_EXHAUSTION_TYPE, PMETypeFailFastOnCommitFailure, PMETypeMax, PPROCESS_MEMORY_EXHAUSTION_TYPE, PPROCESS_MEMORY_EXHAUSTION_TYPE enumeration pointer, PROCESS_MEMORY_EXHAUSTION_TYPE, PROCESS_MEMORY_EXHAUSTION_TYPE enumeration, _PROCESS_MEMORY_EXHAUSTION_TYPE, base.process_memory_exhaustion_type, processthreadsapi/ PMETypeFailFastOnCommitFailure, processthreadsapi/ PMETypeMax, processthreadsapi/PPROCESS_MEMORY_EXHAUSTION_TYPE, processthreadsapi/PROCESS_MEMORY_EXHAUSTION_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - PROCESS_MEMORY_EXHAUSTION_TYPE
product: Windows
targetos: Windows
req.typenames: PROCESS_MEMORY_EXHAUSTION_TYPE, *PPROCESS_MEMORY_EXHAUSTION_TYPE
req.redist: 
---

# _PROCESS_MEMORY_EXHAUSTION_TYPE enumeration


## -description


Represents the different memory exhaustion types.


## -enum-fields




### -field PMETypeFailFastOnCommitFailure

Anytime memory management fails an allocation due to an inability to commit memory, it will cause the process to trigger a Windows Error Reporting report and then terminate immediately with <b>STATUS_COMMITMENT_LIMIT</b>. 
The failure cannot be caught and handled by the app.


### -field PMETypeMax

The maximum value for this enumeration. This value may change in a future version.

