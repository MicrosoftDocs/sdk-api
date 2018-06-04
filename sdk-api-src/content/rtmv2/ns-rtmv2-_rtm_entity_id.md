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

# _RTM_ENTITY_ID structure


## -description


The 
<b>RTM_ENTITY_ID</b> structure is used to uniquely identify a client to the routing table manager. The protocol identifier and the instance identifier are the values that are used to uniquely identify a client.


## -struct-fields




### -field EntityProtocolId

Specifies a client's protocol identifier (such as RIP or OSPF).


### -field EntityInstanceId

Specifies a client's protocol instance (such as RIPv1 or RIPv2).


### -field EntityId

Specifies a client's identifier, which is a combination of the <b>EntityProtocolId</b> and the <b>EntityInstanceId</b>.


## -see-also




<a href="https://msdn.microsoft.com/b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a">RTM_ENTITY_INFO</a>
 

 

