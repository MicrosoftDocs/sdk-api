---
UID: NE:d3d12.D3D12_RTV_DIMENSION
title: D3D12_RTV_DIMENSION
author: windows-sdk-content
description: Identifies the type of resource to view as a render target.
old-location: direct3d12\d3d12_rtv_dimension.htm
tech.root: direct3d12
ms.assetid: 16689D46-D5DC-4119-8148-BCFF0E358D6E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_RTV_DIMENSION, D3D12_RTV_DIMENSION enumeration, D3D12_RTV_DIMENSION_BUFFER, D3D12_RTV_DIMENSION_TEXTURE1D, D3D12_RTV_DIMENSION_TEXTURE1DARRAY, D3D12_RTV_DIMENSION_TEXTURE2D, D3D12_RTV_DIMENSION_TEXTURE2DARRAY, D3D12_RTV_DIMENSION_TEXTURE2DMS, D3D12_RTV_DIMENSION_TEXTURE2DMSARRAY, D3D12_RTV_DIMENSION_TEXTURE3D, D3D12_RTV_DIMENSION_UNKNOWN, d3d12/D3D12_RTV_DIMENSION, d3d12/D3D12_RTV_DIMENSION_BUFFER, d3d12/D3D12_RTV_DIMENSION_TEXTURE1D, d3d12/D3D12_RTV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_RTV_DIMENSION_TEXTURE2D, d3d12/D3D12_RTV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_RTV_DIMENSION_TEXTURE2DMS, d3d12/D3D12_RTV_DIMENSION_TEXTURE2DMSARRAY, d3d12/D3D12_RTV_DIMENSION_TEXTURE3D, d3d12/D3D12_RTV_DIMENSION_UNKNOWN, direct3d12.d3d12_rtv_dimension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - D3D12_RTV_DIMENSION
product: Windows
targetos: Windows
req.typenames: D3D12_RTV_DIMENSION
req.redist: 
---

# D3D12_RTV_DIMENSION enumeration


## -description


Identifies the type of resource to view as a render target.


## -enum-fields




### -field D3D12_RTV_DIMENSION_UNKNOWN

Do not use this value, as it will cause <a href="https://msdn.microsoft.com/B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4">ID3D12Device::CreateRenderTargetView</a> to fail.


### -field D3D12_RTV_DIMENSION_BUFFER

The resource will be accessed as a buffer.


### -field D3D12_RTV_DIMENSION_TEXTURE1D

The resource will be accessed as a 1D texture.


### -field D3D12_RTV_DIMENSION_TEXTURE1DARRAY

The resource will be accessed as an array of 1D textures.


### -field D3D12_RTV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.


### -field D3D12_RTV_DIMENSION_TEXTURE2DARRAY

The resource will be accessed as an array of 2D textures.


### -field D3D12_RTV_DIMENSION_TEXTURE2DMS

The resource will be accessed as a 2D texture with multisampling.


### -field D3D12_RTV_DIMENSION_TEXTURE2DMSARRAY

The resource will be accessed as an array of 2D textures with multisampling.


### -field D3D12_RTV_DIMENSION_TEXTURE3D

The resource will be accessed as a 3D texture.


## -remarks



Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

