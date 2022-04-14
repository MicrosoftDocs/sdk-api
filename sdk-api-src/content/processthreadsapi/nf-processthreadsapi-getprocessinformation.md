---
UID: NF:processthreadsapi.GetProcessInformation
title: GetProcessInformation function (processthreadsapi.h)
description: Retrieves information about the specified process.
helpviewer_keywords: ["GetProcessInformation","GetProcessInformation function","base.getprocessinformation","processthreadsapi/GetProcessInformation"]
old-location: base\getprocessinformation.htm
tech.root: backup
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

A handle to the process. This handle must have the <b>PROCESS_SET_INFORMATION</b> access 
     right. For more information, see 
     <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param ProcessInformationClass [in]

A member of the [PROCESS_INFORMATION_CLASS](./ne-processthreadsapi-process_information_class.md) enumeration specifying the kind of information to retrieve.

### -param ProcessInformation

Pointer to an object to receive the type of information specified by the 
       <i>ProcessInformationClass</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessMemoryPriority</b>, this parameter must point to a 
       <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must point to a 
       <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_power_throttling_state">PROCESS_POWER_THROTTLING_STATE</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessProtectionLevelInfo</b>, this parameter must point to a 
       <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-process_protection_level_information">PROCESS_PROTECTION_LEVEL_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must point to a 
       <a href="../processthreadsapi/ns-processthreadsapi-process_leap_second_info.md">PROCESS_LEAP_SECOND_INFO</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessAppMemoryInfo</b>, this parameter must point to a 
       <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information">APP_MEMORY_INFORMATION</a> structure.

### -param ProcessInformationSize [in]

The size in bytes of the structure specified by the <i>ProcessInformation</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
      <b>ProcessMemoryPriority</b>, this parameter must be 
      <code>sizeof(MEMORY_PRIORITY_INFORMATION)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessProtectionLevelInfo</b>, this parameter must be 
       <code>sizeof(PROCESS_PROTECTION_LEVEL_INFORMATION)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must be 
       <code>sizeof(PROCESS_LEAP_SECOND_INFO)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessAppMemoryInfo</b>, this parameter must be 
       <code>sizeof(APP_MEMORY_INFORMATION)</code>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadinformation">GetThreadInformation</a>



<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a>



<a href="/previous-versions/mt767996(v=vs.85)">PROCESS_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a>
