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

# GetCurrentThreadStackLimits function


## -description


Retrieves the boundaries of the stack that was allocated by the system for the current thread.


## -parameters




### -param LowLimit [out]

A pointer variable that receives the lower boundary of the current thread stack.


### -param HighLimit [out]

A pointer variable that receives the upper boundary of the current thread stack.


## -returns



This function does not return a value.




## -remarks



    It is possible for user-mode code to execute in stack memory
         that is outside the region allocated by the system when the thread was created. Callers
         can use the <b>GetCurrentThreadStackLimits</b> function to verify that the current stack pointer is within the returned
         limits.


To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0602. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>. 




## -see-also




<a href="https://msdn.microsoft.com/abb2d5c1-040b-4c36-aae5-3517b6a8c540">Thread Stack Size</a>
 

 

