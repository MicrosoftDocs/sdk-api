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

# D3D12_TEXTURE_COPY_TYPE enumeration


## -description


Specifies what type of texture copy is to take place.


## -enum-fields




### -field D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX

Indicates a subresource, identified by an index, is to be copied.


### -field D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT

Indicates a place footprint, identified by a <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structure, is to be copied.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/D63EC731-EE75-44CD-9CCD-7FB4A761D1A3">D3D12_TEXTURE_COPY_LOCATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

