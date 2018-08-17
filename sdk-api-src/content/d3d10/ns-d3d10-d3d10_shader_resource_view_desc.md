---
UID: NS:d3d10.D3D10_SHADER_RESOURCE_VIEW_DESC
title: D3D10_SHADER_RESOURCE_VIEW_DESC
author: windows-sdk-content
description: Describes a shader-resource view.
old-location: direct3d10\d3d10_shader_resource_view_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_resource_view_desc.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 7ae3bb9d-8153-8ae3-c7bb-4b1581c7af45, D3D10_SHADER_RESOURCE_VIEW_DESC, D3D10_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 10], d3d10/D3D10_SHADER_RESOURCE_VIEW_DESC, direct3d10.d3d10_shader_resource_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
req.include-header: D3D10Shader.h
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
req.typenames: D3D10_SHADER_RESOURCE_VIEW_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10.h
api_name:
 - D3D10_SHADER_RESOURCE_VIEW_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_SHADER_RESOURCE_VIEW_DESC structure


## -description


Describes a shader-resource view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

The viewing <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">format</a>. See remarks.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/2c2a6a68-179a-478b-bd86-c023a387601d">D3D10_SRV_DIMENSION</a></b>

The resource type of the view. See <a href="https://msdn.microsoft.com/2c2a6a68-179a-478b-bd86-c023a387601d">D3D10_SRV_DIMENSION</a>. This should be the same as the resource type of the underlying resource. This parameter also determines which _SRV to use in the union below.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204898(v=VS.85).aspx">D3D10_BUFFER_SRV</a></b>

View the resource as a buffer using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb204898(v=VS.85).aspx">D3D10_BUFFER_SRV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172463(v=VS.85).aspx">D3D10_TEX1D_SRV</a></b>

View the resource as a 1D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172463(v=VS.85).aspx">D3D10_TEX1D_SRV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172460(v=VS.85).aspx">D3D10_TEX1D_ARRAY_SRV</a></b>

View the resource as a 1D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172460(v=VS.85).aspx">D3D10_TEX1D_ARRAY_SRV</a>.


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172475(v=VS.85).aspx">D3D10_TEX2D_SRV</a></b>

View the resource as a 2D-texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172475(v=VS.85).aspx">D3D10_TEX2D_SRV</a>.


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172472(v=VS.85).aspx">D3D10_TEX2D_ARRAY_SRV</a></b>

View the resource as a 2D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172472(v=VS.85).aspx">D3D10_TEX2D_ARRAY_SRV</a>.


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172469(v=VS.85).aspx">D3D10_TEX2DMS_SRV</a></b>

View the resource as a 2D-multisampled texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172469(v=VS.85).aspx">D3D10_TEX2DMS_SRV</a>.


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172466(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_SRV</a></b>

View the resource as a 2D-multisampled-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172466(v=VS.85).aspx">D3D10_TEX2DMS_ARRAY_SRV</a>.


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172477(v=VS.85).aspx">D3D10_TEX3D_SRV</a></b>

View the resource as a 3D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172477(v=VS.85).aspx">D3D10_TEX3D_SRV</a>.


### -field TextureCube

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172478(v=VS.85).aspx">D3D10_TEXCUBE_SRV</a></b>

View the resource as a 3D-cube texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/en-us/library/Bb172478(v=VS.85).aspx">D3D10_TEXCUBE_SRV</a>).


## -remarks



A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read. For more information about how views work, see <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">Views</a>


When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173558(v=VS.85).aspx">ID3D10Device::CreateShaderResourceView</a>. To view a shader-resource-view description, call <a href="https://msdn.microsoft.com/en-us/library/Bb173855(v=VS.85).aspx">ID3D10ShaderResourceView::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205153(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

