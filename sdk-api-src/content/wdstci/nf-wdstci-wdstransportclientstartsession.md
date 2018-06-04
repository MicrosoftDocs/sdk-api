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

# WdsTransportClientStartSession function


## -description


Initiates a multicast file transfer.


## -parameters




### -param hSessionKey [in]

The handle returned by the <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a> session.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



All callbacks must be registered before this function is called.  If a required callback is not registered, this function will fail.

It is possible for a session to start and complete before this function  returns. This means that it is possible to receive a callback with a session handle that has not been seen yet.  This also means that a session can start and error out before this function has a chance to complete.  In this case, this function may still return success, even if the session itself fails.



