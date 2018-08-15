---
UID: NE:d3d12.D3D12_DSV_DIMENSION
title: D3D12_DSV_DIMENSION
author: windows-sdk-content
description: Specifies how to access a resource used in a depth-stencil view.
old-location: direct3d12\d3d12_dsv_dimension.htm
old-project: direct3d12
ms.assetid: 87ABAD56-E5EE-4F96-87DC-D1EB485B621D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_DSV_DIMENSION, D3D12_DSV_DIMENSION enumeration, D3D12_DSV_DIMENSION_TEXTURE1D, D3D12_DSV_DIMENSION_TEXTURE1DARRAY, D3D12_DSV_DIMENSION_TEXTURE2D, D3D12_DSV_DIMENSION_TEXTURE2DARRAY, D3D12_DSV_DIMENSION_TEXTURE2DMS, D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY, D3D12_DSV_DIMENSION_UNKNOWN, d3d12/D3D12_DSV_DIMENSION, d3d12/D3D12_DSV_DIMENSION_TEXTURE1D, d3d12/D3D12_DSV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_DSV_DIMENSION_TEXTURE2D, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMS, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY, d3d12/D3D12_DSV_DIMENSION_UNKNOWN, direct3d12.d3d12_dsv_dimension
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
req.typenames: D3D12_DSV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DSV_DIMENSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_DSV_DIMENSION enumeration


## -description


Specifies how to access a resource used in a depth-stencil view.


## -enum-fields




### -field D3D12_DSV_DIMENSION_UNKNOWN

<b>D3D12_DSV_DIMENSION_UNKNOWN</b> is not a valid value for <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> and is not used.


### -field D3D12_DSV_DIMENSION_TEXTURE1D

The resource will be accessed as a 1D texture.


### -field D3D12_DSV_DIMENSION_TEXTURE1DARRAY

The resource will be accessed as an array of 1D textures.


### -field D3D12_DSV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.


### -field D3D12_DSV_DIMENSION_TEXTURE2DARRAY

The resource will be accessed as an array of 2D textures.


### -field D3D12_DSV_DIMENSION_TEXTURE2DMS

The resource will be accessed as a 2D texture with multi sampling.


### -field D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY

The resource will be accessed as an array of 2D textures with multi sampling.


## -remarks



Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

