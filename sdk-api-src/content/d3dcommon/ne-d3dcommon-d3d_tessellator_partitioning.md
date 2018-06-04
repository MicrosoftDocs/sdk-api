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

# D3D_TESSELLATOR_PARTITIONING enumeration


## -description


Values that identify partitioning options.


## -enum-fields




### -field D3D_TESSELLATOR_PARTITIONING_UNDEFINED

The partitioning type is undefined.


### -field D3D_TESSELLATOR_PARTITIONING_INTEGER

Partition with integers only.


### -field D3D_TESSELLATOR_PARTITIONING_POW2

Partition with a power-of-two number only.


### -field D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD

Partition with an odd, fractional number.


### -field D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN

Partition with an even, fractional number.


### -field D3D11_TESSELLATOR_PARTITIONING_UNDEFINED

The partitioning type is undefined.


### -field D3D11_TESSELLATOR_PARTITIONING_INTEGER

Partition with integers only.


### -field D3D11_TESSELLATOR_PARTITIONING_POW2

Partition with a power-of-two number only.


### -field D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD

Partition with an odd, fractional number.


### -field D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN

Partition with an even, fractional number.


## -remarks



During tessellation, the partition option helps to determine how the algorithm chooses the next partition value; this enumeration is used by <a href="https://msdn.microsoft.com/25c8f773-e319-4ba1-b332-d45b8323e8c8">D3D11_SHADER_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

