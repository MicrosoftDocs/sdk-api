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

# MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration


## -description



Defines flags for serializing and deserializing attribute stores.




## -enum-fields




### -field MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF

If this flag is set, <b>IUnknown</b> pointers in the attribute store are marshaled to and from the stream. If this flag is absent, <b>IUnknown</b> pointers in the attribute store are not marshaled or serialized.


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a">MFDeserializeAttributesFromStream</a>



<a href="https://msdn.microsoft.com/b8bc88e5-19ae-46b3-aa78-a00afee1f481">MFSerializeAttributesToStream</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

