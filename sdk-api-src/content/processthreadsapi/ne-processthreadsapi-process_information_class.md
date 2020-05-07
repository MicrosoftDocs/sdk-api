---
UID: NE:processthreadsapi._PROCESS_INFORMATION_CLASS
title: PROCESS_INFORMATION_CLASS
ms.date: 05/05/2020
ms.topic: language-reference
targetos: Windows
description: Indicates a specific class of process information.
tech.root: SecAuthZ
req.construct-type: enumeration
req.ddi-compliance: 
req.header: processthreadsapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - _PROCESS_INFORMATION_CLASS
 - PROCESS_INFORMATION_CLASS
f1_keywords:
 - processthreadsapi/_PROCESS_INFORMATION_CLASS
 - processthreadsapi/PROCESS_INFORMATION_CLASS
dev_langs:
 - c++
---

## -description

Indicates a specific class of process information. Values from this enumeration are passed into the [GetProcessInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessinformation) and [SetProcessInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) functions to specify the type of process information passed in the void pointer argument of the function call.

## -enum-fields

### -field ProcessMemoryPriority

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a> structure.

### -field ProcessMemoryExhaustionInfo

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info">PROCESS_MEMORY_EXHAUSTION_INFO</a> structure.

### -field ProcessAppMemoryInfo

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information">APP_MEMORY_INFORMATION</a> structure.

### -field ProcessInPrivateInfo

The process information is ignored. 

### -field ProcessPowerThrottling

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_power_throttling_state">PROCESS_POWER_THROTTLING_STATE</a> structure.

### -field ProcessReservedValue1

Reserved.

### -field ProcessTelemetryCoverageInfo

Reserved.

### -field ProcessProtectionLevelInfo

The process information is represented by a <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-process_protection_level_information">PROCESS_PROTECTION_LEVEL_INFORMATION</a> structure.

### -field ProcessLeapSecondInfo

The process information is represented by a <a href="https://msdn.microsoft.com/en-us/library/Mt829716(v=VS.85).aspx">PROCESS_LEAP_SECOND_INFO</a> structure.

### -field ProcessInformationClassMax

Reserved.

## -remarks

## -see-also

