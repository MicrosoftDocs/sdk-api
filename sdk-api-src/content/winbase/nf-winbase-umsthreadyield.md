---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

