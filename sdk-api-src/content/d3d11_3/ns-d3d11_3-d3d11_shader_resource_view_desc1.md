---
UID: NS:d3d11_3.D3D11_SHADER_RESOURCE_VIEW_DESC1
title: D3D11_SHADER_RESOURCE_VIEW_DESC1
author: windows-sdk-content
description: Describes a shader-resource view.
old-location: direct3d11\d3d11_shader_resource_view_desc1.htm
tech.root: direct3d11
ms.assetid: 051F58C1-E3F3-4205-B834-7A14FEDFED2C
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CD3D11_SHADER_RESOURCE_VIEW_DESC1, D3D11_SHADER_RESOURCE_VIEW_DESC1, D3D11_SHADER_RESOURCE_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_SHADER_RESOURCE_VIEW_DESC1, direct3d11.d3d11_shader_resource_view_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_3.h
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
 - D3D11_3.h
api_name:
 - D3D11_SHADER_RESOURCE_VIEW_DESC1
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_RESOURCE_VIEW_DESC1
req.redist: 
---

# D3D11_SHADER_RESOURCE_VIEW_DESC1 structure


## -description


Describes a shader-resource view.


## -struct-fields




#### - Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that  specifies the viewing format. See remarks.


#### - ViewDimension

A <a href="https://msdn.microsoft.com/0b3ae8b9-12fc-4de9-b99d-e9b9e17adfb4">D3D11_SRV_DIMENSION</a>-typed value that  specifies the resource type of the view. This type is the same as the resource type of the underlying resource. This member also determines which _SRV to use in the union below.


#### - Buffer

A <a href="https://msdn.microsoft.com/en-us/library/Ff476094(v=VS.85).aspx">D3D11_BUFFER_SRV</a> structure that views the resource as a buffer.


#### - Texture1D

A <a href="https://msdn.microsoft.com/en-us/library/Ff476231(v=VS.85).aspx">D3D11_TEX1D_SRV</a> structure that views the resource as a 1D texture.


#### - Texture1DArray

A <a href="https://msdn.microsoft.com/en-us/library/Ff476227(v=VS.85).aspx">D3D11_TEX1D_ARRAY_SRV</a> structure that views the resource as a 1D-texture array.


#### - Texture2D

A <a href="https://msdn.microsoft.com/en-us/library/Dn899164(v=VS.85).aspx">D3D11_TEX2D_SRV1</a> structure that views the resource as a 2D-texture.


#### - Texture2DArray

A <a href="https://msdn.microsoft.com/en-us/library/Dn899161(v=VS.85).aspx">D3D11_TEX2D_ARRAY_SRV1</a> structure that views the resource as a 2D-texture array.


#### - Texture2DMS

A <a href="https://msdn.microsoft.com/en-us/library/Ff476238(v=VS.85).aspx">D3D11_TEX2DMS_SRV</a> structure that views the resource as a 2D-multisampled texture.


#### - Texture2DMSArray

A <a href="https://msdn.microsoft.com/en-us/library/Ff476235(v=VS.85).aspx">D3D11_TEX2DMS_ARRAY_SRV</a> structure that views the resource as a 2D-multisampled-texture array.


#### - Texture3D

A <a href="https://msdn.microsoft.com/en-us/library/Ff476248(v=VS.85).aspx">D3D11_TEX3D_SRV</a> structure that views the resource as a 3D texture.


#### - TextureCube

A <a href="https://msdn.microsoft.com/en-us/library/Ff476251(v=VS.85).aspx">D3D11_TEXCUBE_SRV</a> structure that views the resource as a 3D-cube texture.


#### - TextureCubeArray

A <a href="https://msdn.microsoft.com/en-us/library/Ff476250(v=VS.85).aspx">D3D11_TEXCUBE_ARRAY_SRV</a> structure that views the resource as a 3D-cube-texture array.


#### - BufferEx

A <a href="https://msdn.microsoft.com/en-us/library/Ff476090(v=VS.85).aspx">D3D11_BUFFEREX_SRV</a> structure that views the resource as a raw buffer. For more info about raw viewing of buffers, see <a href="https://msdn.microsoft.com/en-us/library/Ff476900(v=VS.85).aspx">Raw Views of Buffers</a>.


## -remarks



A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.

When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="https://msdn.microsoft.com/en-us/library/Dn899227(v=VS.85).aspx">ID3D11Device3::CreateShaderResourceView1</a>. To view a shader-resource-view description, call <a href="https://msdn.microsoft.com/en-us/library/Dn899243(v=VS.85).aspx">ID3D11ShaderResourceView1::GetDesc1</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

