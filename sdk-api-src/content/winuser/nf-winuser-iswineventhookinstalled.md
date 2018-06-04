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

# IsWinEventHookInstalled function


## -description


Determines whether there is an installed WinEvent hook that might be notified of a specified event.


## -parameters




### -param event [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The event constant that hooks might be notified of. The function checks whether there is an installed hook for this event constant.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If there is a hook to be notified of the specified event, the return value is <b>TRUE</b>.

If there are no hooks to be notified of the specified event, the return value is <b>FALSE</b>.




## -remarks



This method is guaranteed to never return a false negative. If this method returns <b>FALSE</b>, it means that no hooks in the system would be notified of the event. However, this method may return a false positive. In other words, it may return <b>TRUE</b> even though there are no hooks that would be notified. Thus, it is safe for components to circumvent some work if this method returns <b>FALSE</b>. 

Event hooks can be installed at any time, so server developers should not cache the return value for long periods of time.




## -see-also




<a href="https://msdn.microsoft.com/090bda1b-0635-4aa3-ae33-3987b36e30b8">SetWinEventHook</a>



<a href="https://msdn.microsoft.com/5cffb279-85e1-4f7a-8bbb-d0d618f6afcd">UnhookWinEvent</a>
 

 

