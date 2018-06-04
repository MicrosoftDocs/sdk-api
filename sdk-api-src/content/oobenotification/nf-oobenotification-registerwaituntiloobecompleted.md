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

# RegisterWaitUntilOOBECompleted function


## -description


Registers a callback to be called once OOBE (Windows Welcome) has been completed.


## -parameters




### -param OOBECompletedCallback

Pointer to an application-defined callback function that will be called upon completion of OOBE. For more information, see <a href="https://msdn.microsoft.com/9786D6C3-82B1-4546-9BE9-7705AD3B7DBD">OOBE_COMPLETED_CALLBACK</a>.


### -param CallbackContext

Pointer to the callback context. This value will be passed to the function specified by <i>OOBECompletedCallback</i>. This value can be <b>nulll</b>.


### -param WaitHandle

Pointer to a variable that will receive the handle to the wait callback registration.


## -returns



<b>TRUE</b> if the routine successfully registered the callback. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href=" http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> will retrieve extended error information.




## -remarks



If <b>RegisterWaitUntilOOBECompleted</b> returns <b>FALSE</b>, and a subsequent call to <a href=" http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> returns a value of <b>ERROR_INVALID_STATE</b>, this indicates that OOBE is already complete and there is no need to register for OOBE completion.



