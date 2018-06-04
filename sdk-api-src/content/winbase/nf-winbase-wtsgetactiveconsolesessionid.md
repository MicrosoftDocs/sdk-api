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

# WTSGetActiveConsoleSessionId function


## -description


Retrieves the session identifier of the console session. The console session is the session that is currently attached to the physical console. Note that it is not necessary that Remote Desktop Services be running for this 
    function to succeed.


## -parameters






## -returns



The session identifier of the session that is attached to the physical console. If there is no session attached to the 
       physical console, (for example, if the physical console session is in the process of being attached or detached), this function 
       returns 0xFFFFFFFF.




## -remarks



The session identifier returned by this function is the identifier of the current physical console session. To monitor 
    the state of the current physical console session, use the 
    <a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/99a3f047-705c-40bc-8cc2-055257a4f2b3">ProcessIdToSessionId</a>



<a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a>
 

 

