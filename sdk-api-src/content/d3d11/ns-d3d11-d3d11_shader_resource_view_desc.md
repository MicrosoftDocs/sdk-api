---
UID: NS:d3d11.D3D11_SHADER_RESOURCE_VIEW_DESC
title: D3D11_SHADER_RESOURCE_VIEW_DESC
author: windows-sdk-content
description: Describes a shader-resource view.
old-location: direct3d11\d3d11_shader_resource_view_desc.htm
tech.root: direct3d11
ms.assetid: 7ce09172-8a01-4718-b0ef-0ae118a9be16
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 13e27562-b43d-82ba-4ced-1227c27884e5, D3D11_SHADER_RESOURCE_VIEW_DESC, D3D11_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_SHADER_RESOURCE_VIEW_DESC, direct3d11.d3d11_shader_resource_view_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: D3D11Shader.h
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
 - d3d11.h
api_name:
 - D3D11_SHADER_RESOURCE_VIEW_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_RESOURCE_VIEW_DESC
req.redist: 
---

# D3D11_SHADER_RESOURCE_VIEW_DESC structure


## -description


Describes a shader-resource view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> specifying the viewing format. See remarks.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/0b3ae8b9-12fc-4de9-b99d-e9b9e17adfb4">D3D11_SRV_DIMENSION</a></b>

The resource type of the view. See <a href="https://msdn.microsoft.com/0b3ae8b9-12fc-4de9-b99d-e9b9e17adfb4">D3D11_SRV_DIMENSION</a>. This should be the same as the resource type of the underlying resource. This parameter also determines which _SRV to use in the union below.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/2ada8526-bef3-4998-8775-6e062f972a1c">D3D11_BUFFER_SRV</a></b>

View the resource as a buffer using information from a shader-resource view (see <a href="https://msdn.microsoft.com/2ada8526-bef3-4998-8775-6e062f972a1c">D3D11_BUFFER_SRV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a></b>

View the resource as a 1D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/e0caf038-d0d7-4fd4-bec3-f0023035a82a">D3D11_TEX1D_ARRAY_SRV</a></b>

View the resource as a 1D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/e0caf038-d0d7-4fd4-bec3-f0023035a82a">D3D11_TEX1D_ARRAY_SRV</a>).


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/2edfe9bd-6f26-4007-a2bd-0911649e7237">D3D11_TEX2D_SRV</a></b>

View the resource as a 2D-texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/2edfe9bd-6f26-4007-a2bd-0911649e7237">D3D11_TEX2D_SRV</a>).


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/274e7a15-ac54-41e2-87d7-484e3e768a38">D3D11_TEX2D_ARRAY_SRV</a></b>

View the resource as a 2D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/274e7a15-ac54-41e2-87d7-484e3e768a38">D3D11_TEX2D_ARRAY_SRV</a>).


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/ba896737-a94e-49d0-8f35-2e4ef5a335e7">D3D11_TEX2DMS_SRV</a></b>

View the resource as a 2D-multisampled texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/ba896737-a94e-49d0-8f35-2e4ef5a335e7">D3D11_TEX2DMS_SRV</a>).


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/ce020ea2-4b2e-4d80-8ad2-5982cc7ee051">D3D11_TEX2DMS_ARRAY_SRV</a></b>

View the resource as a 2D-multisampled-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/ce020ea2-4b2e-4d80-8ad2-5982cc7ee051">D3D11_TEX2DMS_ARRAY_SRV</a>).


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/d6aacaa5-5314-4ea1-b12e-0ffba850e74c">D3D11_TEX3D_SRV</a></b>

View the resource as a 3D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/d6aacaa5-5314-4ea1-b12e-0ffba850e74c">D3D11_TEX3D_SRV</a>).


### -field TextureCube

Type: <b><a href="https://msdn.microsoft.com/ca320e06-699f-44f9-9a66-93746935b4cd">D3D11_TEXCUBE_SRV</a></b>

View the resource as a 3D-cube texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/ca320e06-699f-44f9-9a66-93746935b4cd">D3D11_TEXCUBE_SRV</a>).


### -field TextureCubeArray

Type: <b><a href="https://msdn.microsoft.com/e8b496a7-89d9-4168-908a-1731ce045851">D3D11_TEXCUBE_ARRAY_SRV</a></b>

View the resource as a 3D-cube-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/e8b496a7-89d9-4168-908a-1731ce045851">D3D11_TEXCUBE_ARRAY_SRV</a>).


### -field BufferEx

Type: <b><a href="https://msdn.microsoft.com/55714c3b-ef21-43c1-94a1-60b63f3fedac">D3D11_BUFFEREX_SRV</a></b>

View the resource as a raw buffer using information from a shader-resource view (see <a href="https://msdn.microsoft.com/55714c3b-ef21-43c1-94a1-60b63f3fedac">D3D11_BUFFEREX_SRV</a>). For more info about raw viewing of buffers, see <a href="overviews_direct3d_11_resources_intro.htm">Raw Views of Buffers</a>.


## -remarks



A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read.

When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="https://msdn.microsoft.com/a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8">ID3D11Device::CreateShaderResourceView</a>. To view a shader-resource-view description, call <a href="https://msdn.microsoft.com/223bcf9c-a873-498c-af58-d93fe0a7f52c">ID3D11ShaderResourceView::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

