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

# _IPX_SERVICE structure


## -description


The 
<b>IPX_SERVICE</b> structure contains information about an IPX service, and identifies the interface and protocol through which this information was obtained.


## -struct-fields




### -field InterfaceIndex

Contains the index of the interface through which the service information was obtained.


### -field Protocol

Contains the identifier of the protocol that obtained the service information. Static services are viewed as services obtained through the IPX_PROTOCOL_STATIC protocol.


### -field Server

 




#### - Service

Specifies an 
<a href="https://msdn.microsoft.com/5b865c28-6a0e-4af3-a646-c1082b5c3ce5">IPX_SERVER_ENTRY</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/5b865c28-6a0e-4af3-a646-c1082b5c3ce5">IPX_SERVER_ENTRY</a>



<a href="https://msdn.microsoft.com/c965c9d5-30bc-4755-b0bf-f59eddfe300d">Service Table Management Structures</a>
 

 

