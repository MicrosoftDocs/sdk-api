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

# EngWaitForSingleObject function


## -description


The <b>EngWaitForSingleObject</b> function puts the current thread of the display driver into a wait state until the specified event object is set to the signaled state, or until the wait times out.


## -parameters




### -param pEvent [in]

Pointer to an initialized event object. This event object handle was obtained in a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>.


### -param pTimeOut [in]

(<i>Optional</i>) Pointer to a time-out value that specifies the absolute or relative time at which the wait is to be completed. A negative value specifies an interval relative to the current time. The value should be expressed in units of 100 nanoseconds. Absolute expiration times track any changes in the system time; relative expiration times are not affected by system time changes. If <i>pTimeOut</i> is <b>NULL</b>, the calling thread remains in a waiting state until the event object is signaled.


## -returns



<b>EngWaitForSingleObject</b> returns <b>TRUE</b> upon success, which includes the occurrence of a time-out. Otherwise, it returns <b>FALSE</b>. A return value of <b>FALSE</b> indicates that one of the parameters is invalid.




## -remarks



<b>EngWaitForSingleObject</b> causes a display driver thread to be put into a wait state. The display driver thread stays in the wait state until either the event object is set to the signaled state or until the wait times out. If no time-out value is supplied, the display driver thread remains in the wait state until the event object is set to the signaled state.

A synchronization event is automatically reset to the nonsignaled state when the wait is satisfied. Thus, only one wait will be satisfied per call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565013">EngSetEvent</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff570364">VideoPortSetEvent</a>. In contrast, a notification event will not be automatically reset.

A time-out value of zero allows the driver to test the wait condition and to conditionally perform any side effects provided that the wait can be immediately satisfied.

The display driver can synchronize drawing operations between itself and the video miniport driver by calling <b>EngWaitForSingleObject</b> with an event object, and waiting until the miniport driver sets the event object to the signaled state.

The driver cannot call <b>EngWaitForSingleObject</b> on events returned from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565013">EngSetEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570364">VideoPortSetEvent</a>
 

 

