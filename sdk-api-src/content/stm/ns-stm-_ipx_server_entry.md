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

# _IPX_SERVER_ENTRY structure


## -description


The 
<b>IPX_SERVER_ENTRY</b> structure describes a particular IPX service.


## -struct-fields




### -field Type

Contains the service type as defined by the SAP specification.


### -field Name

Contains the service name as defined by SAP specifications.


### -field Network

Contains the network number portion of the service address.


### -field Node

Contains the node number portion of the service address.


### -field Socket

Contains the socket number portion of service address.


### -field HopCount

Contains the service hop count.


## -see-also




<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/c965c9d5-30bc-4755-b0bf-f59eddfe300d">Service Table Management Structures</a>
 

 

