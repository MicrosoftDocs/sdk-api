---
UID: NF:winbase.GetProcessIoCounters
title: GetProcessIoCounters function
author: windows-sdk-content
description: Retrieves accounting information for all I/O operations performed by the specified process.
old-location: base\getprocessiocounters.htm
old-project: ProcThread
ms.assetid: e6973c1b-86bc-4fd1-aff6-26e87f8013c4
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetProcessIoCounters, GetProcessIoCounters function, _win32_getprocessiocounters, base.getprocessiocounters, winbase/GetProcessIoCounters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-processtopology-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
api_name:
 - GetProcessIoCounters
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetProcessIoCounters function


## -description


Retrieves accounting information for all I/O operations performed by the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


### -param lpIoCounters [out]

A pointer to an 
<a href="https://msdn.microsoft.com/78729cbe-5256-4939-a7cc-c393662f8361">IO_COUNTERS</a> structure that receives the I/O accounting information for the process.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/78729cbe-5256-4939-a7cc-c393662f8361">IO_COUNTERS</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

