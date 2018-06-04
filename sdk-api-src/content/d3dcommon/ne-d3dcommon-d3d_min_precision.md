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

# D3D_MIN_PRECISION enumeration


## -description


Values that indicate the minimum desired interpolation precision.


## -enum-fields




### -field D3D_MIN_PRECISION_DEFAULT

Default minimum precision, which is 32-bit precision.


### -field D3D_MIN_PRECISION_FLOAT_16

Minimum precision is min16float, which is 16-bit floating point. 


### -field D3D_MIN_PRECISION_FLOAT_2_8

Minimum precision is min10float, which is 10-bit floating point. 


### -field D3D_MIN_PRECISION_RESERVED

Reserved


### -field D3D_MIN_PRECISION_SINT_16

Minimum precision is min16int, which is 16-bit signed integer. 


### -field D3D_MIN_PRECISION_UINT_16

Minimum precision is min16uint, which is 16-bit unsigned integer. 


### -field D3D_MIN_PRECISION_ANY_16

Minimum precision is any 16-bit value. 


### -field D3D_MIN_PRECISION_ANY_10

Minimum precision is any 10-bit value. 


## -remarks



For more info, see <a href="https://msdn.microsoft.com/bf24d27f-2720-4268-bc74-fc46afedb9aa">Scalar Types</a> and <a href="https://msdn.microsoft.com/422B0C45-5CEB-4235-AD05-62D36C36CFC6">Using HLSL minimum precision</a>.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

