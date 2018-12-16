---
UID: NF:winbase.UmsThreadYield
title: UmsThreadYield function
author: windows-sdk-content
description: Yields control to the user-mode scheduling (UMS) scheduler thread on which the calling UMS worker thread is running.
old-location: base\umsthreadyield.htm
tech.root: procthread
ms.assetid: d7c94ed5-9536-4c39-8658-27e4237cc9ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UmsThreadYield, UmsThreadYield function, base.umsthreadyield, winbase/UmsThreadYield
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - UmsThreadYield
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UmsThreadYield function


## -description


Yields control to the user-mode scheduling (UMS) scheduler thread on which the calling UMS worker thread is running.


## -parameters




### -param SchedulerParam [in]

A parameter to pass to the scheduler thread's <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a> function.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A UMS worker thread calls the <b>UmsThreadYield</b> function to cooperatively yield control to the UMS scheduler thread on which the worker thread is running. If a UMS worker thread never calls <b>UmsThreadYield</b>, the worker thread runs until it either blocks or is terminated.

When control switches to the UMS scheduler thread, the system calls the associated scheduler entry point function with the reason <b>UmsSchedulerThreadYield</b> and the <i>ScheduleParam</i> parameter specified by the worker thread in the <b>UmsThreadYield</b> call. 

The application's scheduler is responsible for rescheduling the worker thread.




## -see-also




<a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a>
 

 

