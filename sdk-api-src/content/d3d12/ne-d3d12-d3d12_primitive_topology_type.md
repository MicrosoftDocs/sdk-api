---
UID: NE:d3d12.D3D12_PRIMITIVE_TOPOLOGY_TYPE
title: D3D12_PRIMITIVE_TOPOLOGY_TYPE
author: windows-sdk-content
description: Specifies how the pipeline interprets geometry or hull shader input primitives.
old-location: direct3d12\d3d12_primitive_topology_type.htm
old-project: direct3d12
ms.assetid: 3BD4DF5E-EA91-4B2A-AADE-B9AE0E766F63
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration, D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE, D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH, D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT, D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE, D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED, direct3d12.d3d12_primitive_topology_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: D3D12_PRIMITIVE_TOPOLOGY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_PRIMITIVE_TOPOLOGY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

