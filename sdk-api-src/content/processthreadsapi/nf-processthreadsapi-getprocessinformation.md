---
UID: NF:processthreadsapi.GetProcessInformation
title: GetProcessInformation function (processthreadsapi.h)
description: Retrieves information about the specified process. (GetProcessInformation)
helpviewer_keywords: ["GetProcessInformation","GetProcessInformation function","base.getprocessinformation","processthreadsapi/GetProcessInformation"]
old-location: base\getprocessinformation.htm
tech.root: processthreadsapi
ms.assetid: 2b075405-b7b6-4da0-b78d-45eaa9c6c8cd
ms.date: 12/05/2018
ms.keywords: GetProcessInformation, GetProcessInformation function, base.getprocessinformation, processthreadsapi/GetProcessInformation
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessInformation
 - processthreadsapi/GetProcessInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
api_name:
 - GetProcessInformation
---

# GetProcessInformation function

## -description

Retrieves information about the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have at least the **PROCESS_QUERY_LIMITED_INFORMATION** access right. For more information, see [Process Security and Access Rights](/windows/win32/procthread/process-security-and-access-rights).

### -param ProcessInformationClass [in]

A member of the [PROCESS_INFORMATION_CLASS](./ne-processthreadsapi-process_information_class.md) enumeration specifying the kind of information to retrieve.

### -param ProcessInformation

Pointer to an object to receive the type of information specified by the *ProcessInformationClass* parameter.

If the *ProcessInformationClass* parameter is **ProcessMemoryPriority**, this parameter must point to a [MEMORY_PRIORITY_INFORMATION structure](ns-processthreadsapi-memory_priority_information.md).

If the *ProcessInformationClass* parameter is **ProcessPowerThrottling**, this parameter must point to a [PROCESS_POWER_THROTTLING_STATE structure](ns-processthreadsapi-process_power_throttling_state.md).

If the *ProcessInformationClass* parameter is **ProcessProtectionLevelInfo**, this parameter must point to a [PROCESS_PROTECTION_LEVEL_INFORMATION structure](ns-processthreadsapi-process_protection_level_information.md).

If the *ProcessInformationClass* parameter is **ProcessLeapSecondInfo**, this parameter must point to a [PROCESS_LEAP_SECOND_INFO structure](ns-processthreadsapi-process_leap_second_info.md).

If the *ProcessInformationClass* parameter is **ProcessAppMemoryInfo**, this parameter must point to a [APP_MEMORY_INFORMATION structure](ns-processthreadsapi-app_memory_information.md).

If the *ProcessInformationClass* parameter is **ProcessMaxOverridePrefetchParameter**, this parameter must point to an [OVERRIDE_PREFETCH_PARAMETER structure](ns-processthreadsapi-override_prefetch_parameter.md).

### -param ProcessInformationSize [in]

The size in bytes of the structure specified by the *ProcessInformation* parameter.

If the *ProcessInformationClass* parameter is **ProcessMemoryPriority**, this parameter must be `sizeof(MEMORY_PRIORITY_INFORMATION)`.

If the *ProcessInformationClass* parameter is **ProcessPowerThrottling**, this parameter must be `sizeof(PROCESS_POWER_THROTTLING_STATE)`.

If the *ProcessInformationClass* parameter is **ProcessProtectionLevelInfo**, this parameter must be `sizeof(PROCESS_PROTECTION_LEVEL_INFORMATION)`.

If the *ProcessInformationClass* parameter is **ProcessLeapSecondInfo**, this parameter must be `sizeof(PROCESS_LEAP_SECOND_INFO)`.

If the *ProcessInformationClass* parameter is **ProcessAppMemoryInfo**, this parameter must be `sizeof(APP_MEMORY_INFORMATION)`.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError function](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

[GetThreadInformation function](nf-processthreadsapi-getthreadinformation.md), [MEMORY_PRIORITY_INFORMATION structure](ns-processthreadsapi-memory_priority_information.md), [SetProcessInformation function](nf-processthreadsapi-setprocessinformation.md), [PROCESS_INFORMATION_CLASS enumeration](ne-processthreadsapi-process_information_class.md), [OVERRIDE_PREFETCH_PARAMETER structure](ns-processthreadsapi-override_prefetch_parameter.md)
