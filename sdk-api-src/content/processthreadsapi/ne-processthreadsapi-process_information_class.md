---
UID: NE:processthreadsapi._PROCESS_INFORMATION_CLASS
title: PROCESS_INFORMATION_CLASS (processthreadsapi.h)
ms.date: 05/05/2020
targetos: Windows
description: Indicates a specific class of process information.
tech.root: processthreadsapi
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
 - _PROCESS_INFORMATION_CLASS
 - PROCESS_INFORMATION_CLASS
f1_keywords:
 - _PROCESS_INFORMATION_CLASS
 - processthreadsapi/_PROCESS_INFORMATION_CLASS
 - PROCESS_INFORMATION_CLASS
 - processthreadsapi/PROCESS_INFORMATION_CLASS
dev_langs:
 - c++
---

# PROCESS_INFORMATION_CLASS enumeration

## -description

Indicates a specific class of process information. Values from this enumeration are passed into the [GetProcessInformation](./nf-processthreadsapi-getprocessinformation.md) and [SetProcessInformation](./nf-processthreadsapi-setprocessinformation.md) functions to specify the type of process information passed in the void pointer argument of the function call.

## -enum-fields

### -field ProcessMemoryPriority

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a> structure. Allows applications to lower the default memory priority of threads that perform background operations or access files and data that are not expected to be accessed again soon.

### -field ProcessMemoryExhaustionInfo

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info">PROCESS_MEMORY_EXHAUSTION_INFO</a> structure. Allows applications to configure a process to terminate if an allocation fails to commit memory.

### -field ProcessAppMemoryInfo

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information">APP_MEMORY_INFORMATION</a> structure. Allows applications to query the commit usage and the additional commit available to this process. Does not allow the caller to actually get a commit limit.

### -field ProcessInPrivateInfo

If a process is set to **ProcessInPrivate** mode, and a trace session has set the [EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE](../evntrace/ns-evntrace-enable_trace_parameters.md) flag, then the trace session will drop all events from that process.

### -field ProcessPowerThrottling

The process information is represented by a <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_power_throttling_state">PROCESS_POWER_THROTTLING_STATE</a> structure. Allows applications to configure how the system should throttle the target process's activity when managing power.

### -field ProcessReservedValue1

Reserved.

### -field ProcessTelemetryCoverageInfo

Reserved.

### -field ProcessProtectionLevelInfo

The process information is represented by a <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-process_protection_level_information">PROCESS_PROTECTION_LEVEL_INFORMATION</a> structure.

### -field ProcessLeapSecondInfo

The process information is represented by a <a href="../processthreadsapi/ns-processthreadsapi-process_leap_second_info.md">PROCESS_LEAP_SECOND_INFO</a> structure.

### -field ProcessMachineTypeInfo

The process is represented by a [PROCESS_MACHINE_INFORMATION](ns-processthreadsapi-process_machine_information.md) structure.

### -field ProcessOverrideSubsequentPrefetchParameter

Can be used in a call to the [SetProcessInformation function](nf-processthreadsapi-setprocessinformation.md) to set an [OVERRIDE_PREFETCH_PARAMETER structure](ns-processthreadsapi-override_prefetch_parameter.md) for the application that called it. The prefetch parameter is used to differentiate different file access patterns for the same process name.

### -field ProcessMaxOverridePrefetchParameter

Can be used in a call to the [GetProcessInformation function](nf-processthreadsapi-getprocessinformation.md) to query the maximum allowable value (inclusive) for an [OVERRIDE_PREFETCH_PARAMETER structure](ns-processthreadsapi-override_prefetch_parameter.md). (The prefetch parameter is used to differentiate different file access patterns for the same process name.)

### -field ProcessInformationClassMax

The maximum value for this enumeration. This value may change in a future version.

## -remarks

## -see-also

[GetProcessInformation function](nf-processthreadsapi-getprocessinformation.md), [SetProcessInformation function](nf-processthreadsapi-setprocessinformation.md), [APP_MEMORY_INFORMATION structure](ns-processthreadsapi-app_memory_information.md), [PROCESS_MACHINE_INFORMATION structure](ns-processthreadsapi-process_machine_information.md), [PROCESS_MEMORY_EXHAUSTION_INFO structure](ns-processthreadsapi-process_memory_exhaustion_info.md)
