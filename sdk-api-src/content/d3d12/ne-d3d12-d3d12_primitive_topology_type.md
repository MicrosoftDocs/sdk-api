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

# D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration


## -description


Specifies how the pipeline interprets geometry or hull shader input primitives.


## -enum-fields




### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED

The shader has not been initialized with an input primitive type.


### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT

Interpret the input primitive as a point.


### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE

Interpret the input primitive as a line. 


### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE

Interpret the input primitive as a triangle. 


### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH

Interpret the input primitive as a control point patch.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

