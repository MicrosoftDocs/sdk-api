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

# AvRtJoinThreadOrderingGroup function


## -description


Joins client threads to a thread ordering group.


## -parameters




### -param Context [out]

A pointer to a context handle.


### -param ThreadOrderingGuid [in]

A pointer to the unique identifier for the thread ordering group.


### -param Before [in]

The thread order. If this parameter is <b>TRUE</b>, the thread is a predecessor thread that is scheduled to run before the parent thread. If this parameter is <b>FALSE</b>, the thread is a successor thread that is scheduled to run after the parent thread.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The thread encloses the code to be executed during each period within a loop that is controlled by the <a href="https://msdn.microsoft.com/11318ce3-d938-4bb5-adb1-28dd15e8cd80">AvRtWaitOnThreadOrderingGroup</a> function.

A thread can create more than one thread ordering group and join more than one thread ordering group. However, a thread cannot join the same thread ordering group more than one time.

The number of threads that can join a group is limited only by available system resources.




## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 

