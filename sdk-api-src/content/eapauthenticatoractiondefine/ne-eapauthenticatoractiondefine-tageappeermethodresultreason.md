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

# tagEapPeerMethodResultReason enumeration


## -description


Defines the set of results of an EAP authentication session returned by an EAP authenticator method to an EAP peer method.


## -enum-fields




### -field EapPeerMethodResultUnknown

The success or failure of the authentication session is unknown or indeterminate.


### -field EapPeerMethodResultSuccess

Authentication was successful.


### -field EapPeerMethodResultFailure

Authentication failed.


### -field v1_enum




## -remarks



<b>EapPeerMethodResultReason</b> includes <a href="https://msdn.microsoft.com/a30741ff-5d9a-4ebb-8373-97e9116fc64b">network awareness</a> information for wireless devices.




## -see-also




<a href="https://msdn.microsoft.com/e57e8c74-b224-4c01-913b-e41af651acc3">EAPHost Peer Method Enumerations</a>
 

 

