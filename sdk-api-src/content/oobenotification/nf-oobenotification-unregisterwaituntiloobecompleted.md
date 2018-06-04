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

# UnregisterWaitUntilOOBECompleted function


## -description


Unregisters the callback previously registered via <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a>.


## -parameters




### -param WaitHandle

Handle to be unregistered.


## -returns



<b>TRUE</b> if the callback was successfully unregistered. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href=" http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> will retrieve extended error information.



