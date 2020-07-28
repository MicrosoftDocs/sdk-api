---
UID: NE:d3d12.D3D12_SRV_DIMENSION
title: D3D12_SRV_DIMENSION (d3d12.h)
description: Identifies the type of resource that will be viewed as a shader resource.
helpviewer_keywords: ["D3D12_SRV_DIMENSION","D3D12_SRV_DIMENSION enumeration","D3D12_SRV_DIMENSION_BUFFER","D3D12_SRV_DIMENSION_RAYTRACING_ACCELERATION_STRUCTURE","D3D12_SRV_DIMENSION_TEXTURE1D","D3D12_SRV_DIMENSION_TEXTURE1DARRAY","D3D12_SRV_DIMENSION_TEXTURE2D","D3D12_SRV_DIMENSION_TEXTURE2DARRAY","D3D12_SRV_DIMENSION_TEXTURE2DMS","D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY","D3D12_SRV_DIMENSION_TEXTURE3D","D3D12_SRV_DIMENSION_TEXTURECUBE","D3D12_SRV_DIMENSION_TEXTURECUBEARRAY","D3D12_SRV_DIMENSION_UNKNOWN","d3d12/D3D12_SRV_DIMENSION","d3d12/D3D12_SRV_DIMENSION_BUFFER","d3d12/D3D12_SRV_DIMENSION_RAYTRACING_ACCELERATION_STRUCTURE","d3d12/D3D12_SRV_DIMENSION_TEXTURE1D","d3d12/D3D12_SRV_DIMENSION_TEXTURE1DARRAY","d3d12/D3D12_SRV_DIMENSION_TEXTURE2D","d3d12/D3D12_SRV_DIMENSION_TEXTURE2DARRAY","d3d12/D3D12_SRV_DIMENSION_TEXTURE2DMS","d3d12/D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY","d3d12/D3D12_SRV_DIMENSION_TEXTURE3D","d3d12/D3D12_SRV_DIMENSION_TEXTURECUBE","d3d12/D3D12_SRV_DIMENSION_TEXTURECUBEARRAY","d3d12/D3D12_SRV_DIMENSION_UNKNOWN","direct3d12.d3d12_srv_dimension"]
old-location: direct3d12\d3d12_srv_dimension.htm
tech.root: direct3d12
ms.assetid: 1834E70A-4193-4D75-AE47-5C423EACC349
ms.date: 12/05/2018
ms.keywords: D3D12_SRV_DIMENSION, D3D12_SRV_DIMENSION enumeration, D3D12_SRV_DIMENSION_BUFFER, D3D12_SRV_DIMENSION_RAYTRACING_ACCELERATION_STRUCTURE, D3D12_SRV_DIMENSION_TEXTURE1D, D3D12_SRV_DIMENSION_TEXTURE1DARRAY, D3D12_SRV_DIMENSION_TEXTURE2D, D3D12_SRV_DIMENSION_TEXTURE2DARRAY, D3D12_SRV_DIMENSION_TEXTURE2DMS, D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY, D3D12_SRV_DIMENSION_TEXTURE3D, D3D12_SRV_DIMENSION_TEXTURECUBE, D3D12_SRV_DIMENSION_TEXTURECUBEARRAY, D3D12_SRV_DIMENSION_UNKNOWN, d3d12/D3D12_SRV_DIMENSION, d3d12/D3D12_SRV_DIMENSION_BUFFER, d3d12/D3D12_SRV_DIMENSION_RAYTRACING_ACCELERATION_STRUCTURE, d3d12/D3D12_SRV_DIMENSION_TEXTURE1D, d3d12/D3D12_SRV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_SRV_DIMENSION_TEXTURE2D, d3d12/D3D12_SRV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_SRV_DIMENSION_TEXTURE2DMS, d3d12/D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY, d3d12/D3D12_SRV_DIMENSION_TEXTURE3D, d3d12/D3D12_SRV_DIMENSION_TEXTURECUBE, d3d12/D3D12_SRV_DIMENSION_TEXTURECUBEARRAY, d3d12/D3D12_SRV_DIMENSION_UNKNOWN, direct3d12.d3d12_srv_dimension
f1_keywords:
- d3d12/D3D12_SRV_DIMENSION
dev_langs:
- c++
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D12.h
api_name:
- D3D12_SRV_DIMENSION
targetos: Windows
req.typenames: D3D12_SRV_DIMENSION
req.redist: 
ms.custom: 19H1
---

# D3D12_SRV_DIMENSION enumeration


## -description


Identifies the type of resource that will be viewed as a shader resource.


## -enum-fields




### -field D3D12_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D12_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D12_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D12_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D12_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D12_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D12_SRV_DIMENSION_TEXTURECUBEARRAY

The resource is an array of cube textures.


### -field D3D12_SRV_DIMENSION_RAYTRACING_ACCELERATION_STRUCTURE

The resource is a raytracing acceleration structure.


## -remarks



These values are used by a shader-resource-view description, <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

