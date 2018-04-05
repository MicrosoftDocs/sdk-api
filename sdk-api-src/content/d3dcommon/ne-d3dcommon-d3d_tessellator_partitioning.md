---
UID: NE:d3dcommon.D3D_TESSELLATOR_PARTITIONING
title: D3D_TESSELLATOR_PARTITIONING
author: windows-driver-content
description: Values that identify partitioning options.
old-location: direct3d11\d3d_tessellator_partitioning.htm
old-project: direct3d11
ms.assetid: 2a33c1c2-cdd6-48d0-8bd1-a3108c4b9449
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, D3D11_TESSELLATOR_PARTITIONING_INTEGER, D3D11_TESSELLATOR_PARTITIONING_POW2, D3D11_TESSELLATOR_PARTITIONING_UNDEFINED, D3D_TESSELLATOR_PARTITIONING, D3D_TESSELLATOR_PARTITIONING enumeration [Direct3D 11], D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, D3D_TESSELLATOR_PARTITIONING_INTEGER, D3D_TESSELLATOR_PARTITIONING_POW2, D3D_TESSELLATOR_PARTITIONING_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_INTEGER, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_POW2, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_UNDEFINED, d3dcommon/D3D_TESSELLATOR_PARTITIONING, d3dcommon/D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, d3dcommon/D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, d3dcommon/D3D_TESSELLATOR_PARTITIONING_INTEGER, d3dcommon/D3D_TESSELLATOR_PARTITIONING_POW2, d3dcommon/D3D_TESSELLATOR_PARTITIONING_UNDEFINED, direct3d11.d3d_tessellator_partitioning
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dcommon.h
req.include-header: 
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
req.typenames: D3D_TESSELLATOR_PARTITIONING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3DCommon.h
api_name:
-	D3D_TESSELLATOR_PARTITIONING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

