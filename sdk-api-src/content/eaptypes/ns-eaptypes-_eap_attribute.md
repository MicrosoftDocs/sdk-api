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

# _EAP_ATTRIBUTE structure


## -description


 The <b>EAP_ATTRIBUTE</b> structure contains an EAP attribute.


## -struct-fields




### -field eaType

 


### -field dwLength

The size, in bytes, of <b>pValue</b>.


### -field pValue.size_is

 


### -field pValue.size_is.dwLength

 


### -field pValue

Pointer to a byte buffer that contains the data value of the attribute.


#### - eapType

An <a href="https://msdn.microsoft.com/1c6999f5-b455-4a8d-9967-dc27938e8737">EAP_ATTRIBUTE_TYPE</a> enumeration value that describes the type of the EAP attribute value supplied in <b>pValue</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a>
 

 

