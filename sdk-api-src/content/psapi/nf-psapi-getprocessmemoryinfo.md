---
UID: NF:psapi.GetProcessMemoryInfo
title: GetProcessMemoryInfo function
author: windows-sdk-content
description: Retrieves information about the memory usage of the specified process.
old-location: psapi\getprocessmemoryinfo.htm
tech.root: psapi
ms.assetid: 12990e8d-6097-4502-824e-db6c3f76c715
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProcessMemoryInfo, GetProcessMemoryInfo function [PSAPI], K32GetProcessMemoryInfo, _win32_getprocessmemoryinfo, base.getprocessmemoryinfo, psapi.getprocessmemoryinfo, psapi/GetProcessMemoryInfo, psapi/K32GetProcessMemoryInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - GetProcessMemoryInfo
 - K32GetProcessMemoryInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetProcessMemoryInfo
: 
---

# GetProcessMemoryInfo function


## -description


Retrieves information about the memory usage of the specified process.


## -parameters




### -param Process [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right and the <b>PROCESS_VM_READ</b> access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights.


### -param ppsmemCounters [out]

A pointer to the 
<a href="https://msdn.microsoft.com/288b5865-28a3-478b-ad32-c710fe4f3a81">PROCESS_MEMORY_COUNTERS</a> or <a href="https://msdn.microsoft.com/cf06445d-b71a-4320-afc8-4bd88ebfb284">PROCESS_MEMORY_COUNTERS_EX</a> structure that receives information about the memory usage of the process.


### -param cb [in]

The size of the 
<i>ppsmemCounters</i> structure, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetProcessMemoryInfo</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetProcessMemoryInfo</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetProcessMemoryInfo</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetProcessMemoryInfo</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/23641bf8-3653-4cb9-8008-cd99137ca268">Collecting Memory Usage Information for a Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>



<a href="https://msdn.microsoft.com/288b5865-28a3-478b-ad32-c710fe4f3a81">PROCESS_MEMORY_COUNTERS</a>



<a href="https://msdn.microsoft.com/cf06445d-b71a-4320-afc8-4bd88ebfb284">PROCESS_MEMORY_COUNTERS_EX</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>



<a href="https://msdn.microsoft.com/683c899e-a7e8-4440-8f13-2a713c1618bf">Process Memory Usage Information</a>
 

 

