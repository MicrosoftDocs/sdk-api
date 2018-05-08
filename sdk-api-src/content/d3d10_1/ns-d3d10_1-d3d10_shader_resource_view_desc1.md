---
UID: NS:d3d10_1.D3D10_SHADER_RESOURCE_VIEW_DESC1
title: D3D10_SHADER_RESOURCE_VIEW_DESC1
author: windows-driver-content
description: Describes a shader-resource view.
old-location: direct3d10\d3d10_shader_resource_view_desc1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_resource_view_desc1.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 7b42f6ed-d20a-945b-ecb4-4ba1aa8d083c, D3D10_SHADER_RESOURCE_VIEW_DESC1, D3D10_SHADER_RESOURCE_VIEW_DESC1 structure [Direct3D 10], d3d10_1/D3D10_SHADER_RESOURCE_VIEW_DESC1, direct3d10.d3d10_shader_resource_view_desc1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10_1.h
req.include-header: D3D10_1Shader.h
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
req.typenames: D3D10_SHADER_RESOURCE_VIEW_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d10_1.h
api_name:
-	D3D10_SHADER_RESOURCE_VIEW_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_SHADER_RESOURCE_VIEW_DESC1 structure


## -description


Describes a shader-resource view.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The viewing <a href="https://msdn.microsoft.com/library/windows/hardware/dn922919">format</a>. See remarks.


### -field ViewDimension

Type: <b><a href="https://msdn.microsoft.com/0150d0f0-c8c2-4ac5-a702-8e6cdbe984e5">D3D10_SRV_DIMENSION1</a></b>

The resource type of the view. See <a href="https://msdn.microsoft.com/0150d0f0-c8c2-4ac5-a702-8e6cdbe984e5">D3D10_SRV_DIMENSION1</a>. This should be the same as the resource type of the underlying resource. This parameter also determines which _SRV to use in the union below.


### -field Buffer

Type: <b><a href="https://msdn.microsoft.com/9b43f2c1-7b5d-4b86-9640-9e347765519b">D3D10_BUFFER_SRV</a></b>

View the resource as a buffer using information from a shader-resource view (see <a href="https://msdn.microsoft.com/9b43f2c1-7b5d-4b86-9640-9e347765519b">D3D10_BUFFER_SRV</a>).


### -field Texture1D

Type: <b><a href="https://msdn.microsoft.com/be75a2ad-9beb-4382-b9e7-b95f61b9f632">D3D10_TEX1D_SRV</a></b>

View the resource as a 1D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/be75a2ad-9beb-4382-b9e7-b95f61b9f632">D3D10_TEX1D_SRV</a>).


### -field Texture1DArray

Type: <b><a href="https://msdn.microsoft.com/6c016137-4c0f-4ef8-9a2c-8c4c749d1d44">D3D10_TEX1D_ARRAY_SRV</a></b>

View the resource as a 1D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/6c016137-4c0f-4ef8-9a2c-8c4c749d1d44">D3D10_TEX1D_ARRAY_SRV</a>.


### -field Texture2D

Type: <b><a href="https://msdn.microsoft.com/f567e9a6-90b9-4eb7-b50c-928846d6c3bc">D3D10_TEX2D_SRV</a></b>

View the resource as a 2D-texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/f567e9a6-90b9-4eb7-b50c-928846d6c3bc">D3D10_TEX2D_SRV</a>.


### -field Texture2DArray

Type: <b><a href="https://msdn.microsoft.com/0382f49e-8021-4c45-b2a2-3f2a6951b444">D3D10_TEX2D_ARRAY_SRV</a></b>

View the resource as a 2D-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/0382f49e-8021-4c45-b2a2-3f2a6951b444">D3D10_TEX2D_ARRAY_SRV</a>.


### -field Texture2DMS

Type: <b><a href="https://msdn.microsoft.com/1081fc21-46ab-4685-aeda-3af40f41a330">D3D10_TEX2DMS_SRV</a></b>

View the resource as a 2D-multisampled texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/1081fc21-46ab-4685-aeda-3af40f41a330">D3D10_TEX2DMS_SRV</a>.


### -field Texture2DMSArray

Type: <b><a href="https://msdn.microsoft.com/c41109ef-9f23-441a-9c08-60b791580c16">D3D10_TEX2DMS_ARRAY_SRV</a></b>

View the resource as a 2D-multisampled-texture array using information from a shader-resource view (see <a href="https://msdn.microsoft.com/c41109ef-9f23-441a-9c08-60b791580c16">D3D10_TEX2DMS_ARRAY_SRV</a>.


### -field Texture3D

Type: <b><a href="https://msdn.microsoft.com/0e4b1785-d40a-42a7-959d-3a2fcddcf0ed">D3D10_TEX3D_SRV</a></b>

View the resource as a 3D texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/0e4b1785-d40a-42a7-959d-3a2fcddcf0ed">D3D10_TEX3D_SRV</a>.


### -field TextureCube

Type: <b><a href="https://msdn.microsoft.com/98e405d0-9a84-41b5-b647-cce29569da96">D3D10_TEXCUBE_SRV</a></b>

View the resource as a 3D-cube texture using information from a shader-resource view (see <a href="https://msdn.microsoft.com/98e405d0-9a84-41b5-b647-cce29569da96">D3D10_TEXCUBE_SRV</a>).

Type: <b><a href="https://msdn.microsoft.com/441b69d6-df76-4995-815a-a08405203fef">D3D10_TEXCUBE_ARRAY_SRV1</a></b>

View the resource as an array of cube textures using information from a shader-resource view (see <a href="https://msdn.microsoft.com/441b69d6-df76-4995-815a-a08405203fef">D3D10_TEXCUBE_ARRAY_SRV1</a>).


### -field TextureCubeArray

 




## -remarks



A view is a format-specific way to look at the data in a resource. The view determines what data to look at, and how it is cast when read. For more information about how views work, see <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">Views</a>


When viewing a resource, the resource-view description must specify a typed format, that is compatible with the resource format. So that means that you cannot create a resource-view description using any format with _TYPELESS in the name. You can however view a typeless resource by specifying a typed format for the view. For example, a DXGI_FORMAT_R32G32B32_TYPELESS resource can be viewed with one of these typed formats: DXGI_FORMAT_R32G32B32_FLOAT, DXGI_FORMAT_R32G32B32_UINT, and DXGI_FORMAT_R32G32B32_SINT, since these typed formats are compatible with the typeless resource.

Create a shader-resource-view description by calling <a href="https://msdn.microsoft.com/10a2ffe7-fb5b-4ba9-8b61-5a37b901b514">ID3D10Device1::CreateShaderResourceView1</a>. To view a shader-resource-view description, call <a href="https://msdn.microsoft.com/29550424-d1a3-4ce4-87b0-bd2be4f465fe">ID3D10ShaderResourceView::GetDesc</a>.

This structure requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>



<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

