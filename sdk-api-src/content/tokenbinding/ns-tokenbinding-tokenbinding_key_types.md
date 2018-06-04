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

# TOKENBINDING_KEY_TYPES structure


## -description


Contains all of the combinations of  types of token binding keys that a client device or server supports.


## -struct-fields




### -field keyCount

The number of elements in the array that the <b>key</b> member contains.


### -field keyType

 




#### - key

An array of all of the combinations of  types of token binding keys that a client device or server supports. These keys map one-to-one to Application Layer Protocol Negotiation (ALPN) protocol identifiers. You must maintain the table of these mappings.


## -see-also




<a href="https://msdn.microsoft.com/583687B6-5A87-4616-A5EE-4FECFF06749E">TokenBindingGetKeyTypesClient</a>



<a href="https://msdn.microsoft.com/8ABAC0AF-AF68-4742-9C36-3FB17D303409">TokenBindingGetKeyTypesServer</a>
 

 

