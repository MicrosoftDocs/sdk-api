---
UID: NF:processthreadsapi.GetProcessHandleCount
title: GetProcessHandleCount function
author: windows-sdk-content
description: Retrieves the number of open handles that belong to the specified process.
old-location: base\getprocesshandlecount.htm
old-project: procthread
ms.assetid: bb8cf86b-00b8-4a64-90f8-66ac6dbf9dee
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProcessHandleCount, GetProcessHandleCount function, base.getprocesshandlecount, processthreadsapi/GetProcessHandleCount, winbase/GetProcessHandleCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetProcessHandleCount
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# GetProcessHandleCount function


## -description


Retrieves the number of open handles  that belong to the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose handle count is being requested.  The
        handle must have the PROCESS_QUERY_INFORMATION
        or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.


### -param pdwHandleCount [in, out]

A pointer to a variable that receives the number of open handles that belong to the specified process.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error  information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function retrieves information about the executive objects for the process. For more information, see <a href="https://msdn.microsoft.com/3e3288dd-155a-41d0-9d43-5f49ed4c4a9d">Kernel Objects</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

