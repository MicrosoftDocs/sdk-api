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

# D3D_SRV_DIMENSION enumeration


## -description


Values that identify the type of resource to be viewed as a shader resource.


## -enum-fields




### -field D3D_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D_SRV_DIMENSION_TEXTURECUBEARRAY

The resource is an array of cube textures.


### -field D3D_SRV_DIMENSION_BUFFEREX

The resource is a raw buffer. For more info about raw viewing of buffers, see <a href="overviews_direct3d_11_resources_intro.htm">Raw Views of Buffers</a>.


### -field D3D10_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D10_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D10_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D10_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D10_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D10_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D10_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D10_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D10_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D10_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D10_1_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D10_1_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D10_1_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D10_1_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D10_1_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D10_1_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D10_1_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D10_1_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D10_1_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D10_1_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D10_1_SRV_DIMENSION_TEXTURECUBEARRAY

The resource is an array of cube textures.


### -field D3D11_SRV_DIMENSION_UNKNOWN

The type is unknown.


### -field D3D11_SRV_DIMENSION_BUFFER

The resource is a buffer.


### -field D3D11_SRV_DIMENSION_TEXTURE1D

The resource is a 1D texture.


### -field D3D11_SRV_DIMENSION_TEXTURE1DARRAY

The resource is an array of 1D textures.


### -field D3D11_SRV_DIMENSION_TEXTURE2D

The resource is a 2D texture.


### -field D3D11_SRV_DIMENSION_TEXTURE2DARRAY

The resource is an array of 2D textures.


### -field D3D11_SRV_DIMENSION_TEXTURE2DMS

The resource is a multisampling 2D texture.


### -field D3D11_SRV_DIMENSION_TEXTURE2DMSARRAY

The resource is an array of multisampling 2D textures.


### -field D3D11_SRV_DIMENSION_TEXTURE3D

The resource is a 3D texture.


### -field D3D11_SRV_DIMENSION_TEXTURECUBE

The resource is a cube texture.


### -field D3D11_SRV_DIMENSION_TEXTURECUBEARRAY

The resource is an array of cube textures.


### -field D3D11_SRV_DIMENSION_BUFFEREX

The resource is a raw buffer. For more info about raw viewing of buffers, see <a href="overviews_direct3d_11_resources_intro.htm">Raw Views of Buffers</a>.


## -remarks



A <b>D3D_SRV_DIMENSION</b>-typed value is specified in the <b>ViewDimension</b> member of the <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a> structure or the  <b>Dimension</b> member of the <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

