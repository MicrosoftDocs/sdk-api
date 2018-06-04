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

# _ISOLATION_STATE enumeration


## -description


Defines the set of possible isolation state values of a machine.  The isolation state of a machine determines its network connectivity.


## -enum-fields




### -field ISOLATION_STATE_UNKNOWN

The client's access to the network is unknown.


### -field ISOLATION_STATE_NOT_RESTRICTED

The client has unrestricted full access to the network.


### -field ISOLATION_STATE_IN_PROBATION

The client has probationary access to the network for a limited amount of time during which time they must fix their system.


### -field ISOLATION_STATE_RESTRICTED_ACCESS

The client has restricted access to the network; the client is allowed access to some servers only from which they can obtain necessary information and patches to update themselves to become healthy. 


### -field v1_enum




## -remarks



Network Access Protection (NAP) uses the <b>ISOLATION_STATE</b> value to determine if a client should be granted  network access.




## -see-also




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/298c89d9-7a6a-4280-9af9-77c7c00cab92">Implementing In-Band NAP Support for EAP Methods</a>



<a href="https://msdn.microsoft.com/c25e4f03-759a-47a7-8b35-bbe669501c5c">Implementing NAP Support for EAP Methods</a>



<a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">NAP IsolationState</a>



<a href="https://msdn.microsoft.com/7fa12cb4-694a-4db6-9743-5a2cbb995721">NotificationHandler</a>
 

 

