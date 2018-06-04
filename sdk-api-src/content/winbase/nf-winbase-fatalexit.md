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

# FatalExit function


## -description


Transfers execution control to the debugger. The behavior of the debugger thereafter is specific to the type of debugger used.


## -parameters




### -param ExitCode [in]

The error code associated with the exit.


## -returns



This function does not return a value.




## -remarks



An application should only use 
<b>FatalExit</b> for debugging purposes. It should not call the function in a retail version of the application because doing so will terminate the application.




## -see-also




<a href="https://msdn.microsoft.com/d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f">Communicating with the Debugger</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/f18d8b16-ffe1-49f1-98be-ba8d49db86ef">FatalAppExit</a>
 

 

