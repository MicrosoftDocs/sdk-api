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

# SCardAccessStartedEvent function


## -description


The <b>SCardAccessStartedEvent</b> function returns an event handle when an event signals that the smart card resource manager is started. The event-object handle can be specified in a call to one of the wait functions.


## -parameters






## -returns



The function returns an event HANDLE if it succeeds or <b>NULL</b> if it fails.

 If the function fails, the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function provides information on the cause of the failure. 




## -remarks



The event-object handle returned can be specified in a call to one of the wait functions.

Do not close the handle returned by this function.
When you have finished using the handle, decrement the reference count by calling the <a href="https://msdn.microsoft.com/2c08500f-3ebf-4267-8436-b67543e1c13c">SCardReleaseStartedEvent</a> function.



