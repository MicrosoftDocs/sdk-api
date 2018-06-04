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

# IWdsTransportMulticastSessionPolicy::get_AutoDisconnectThreshold


## -description


Sets or retrieves  the threshold transmission rate, in kilobytes per second, used by the server.  If the server  has been configured to handle slow clients using the auto-disconnect method, the server disconnects clients that slow the transmission rate below this threshold value.

This property can be used to get or set the value of the threshold transmission rate regardless of which method the server is using to handle  slow clients.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/bb6677d6-7c60-486a-825a-bafec1f3ffed">IWdsTransportMulticastSessionPolicy</a>
 

 

