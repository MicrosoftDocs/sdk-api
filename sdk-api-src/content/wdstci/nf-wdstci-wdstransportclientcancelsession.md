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

# WdsTransportClientCancelSession function


## -description


Releases the resources associated with a session in the client.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.  This session will eventually complete with an error code of <b>ERROR_CANCELLED</b> to the callback <a href="https://msdn.microsoft.com/1c7b8137-bf74-486c-a90e-6becfec5ddc8">PFN_WdsTransportClientSessionComplete</a> callback.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



It is safe to call this function from within a callback.



