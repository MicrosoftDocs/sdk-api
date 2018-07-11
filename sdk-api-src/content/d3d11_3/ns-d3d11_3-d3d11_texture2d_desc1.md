---
UID: NS:d3d11_3.D3D11_TEXTURE2D_DESC1
title: D3D11_TEXTURE2D_DESC1
author: windows-sdk-content
description: Describes a 2D texture.
old-location: direct3d11\d3d11_texture2d_desc1.htm
old-project: direct3d11
ms.assetid: DADDC12C-CF1E-48B4-B8C0-3029EC6B711B
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: CD3D11_TEXTURE2D_DESC1, D3D11_TEXTURE2D_DESC1, D3D11_TEXTURE2D_DESC1 structure [Direct3D 11], d3d11_3/D3D11_TEXTURE2D_DESC1, direct3d11.d3d11_texture2d_desc1
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
tech.root: 
req.typenames: D3D11_TEXTURE2D_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_TEXTURE2D_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEXTURE2D_DESC1 structure


## -description


Describes a 2D texture.


## -struct-fields




#### - Width

Texture width (in texels). The  range is from 1 to D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION (16384). For a texture cube-map, the  range is from 1 to D3D11_REQ_TEXTURECUBE_DIMENSION (16384). However, the range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


#### - Height

Texture height (in texels). The  range is from 1 to D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION (16384). For a texture cube-map, the  range is from 1 to D3D11_REQ_TEXTURECUBE_DIMENSION (16384). However, the range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


#### - MipLevels

The maximum number of mipmap levels in the texture. See the remarks in <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>. Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


#### - ArraySize

Number of textures in the texture array. The  range is from 1 to D3D11_REQ_TEXTURE2D_ARRAY_AXIS_DIMENSION (2048). For a texture cube-map, this value is a multiple of 6 (that is, 6 times the value in the <b>NumCubes</b> member of <a href="https://msdn.microsoft.com/e8b496a7-89d9-4168-908a-1731ce045851">D3D11_TEXCUBE_ARRAY_SRV</a>), and the  range is from 6 to 2046. The range is actually constrained by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


#### - Format

Texture format (see <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>).


#### - SampleDesc

Structure that specifies multisampling parameters for the texture. See <a href="https://msdn.microsoft.com/a8071d3c-dc78-43fe-84f6-421418e16b02">DXGI_SAMPLE_DESC</a>.


#### - Usage

Value that identifies how the texture is to be read from and written to. The most common value is D3D11_USAGE_DEFAULT; see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a> for all possible values.


#### - BindFlags

Flags (see <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>) for binding to pipeline stages. The flags can be combined by a logical OR.


#### - CPUAccessFlags

Flags (see <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.


#### - MiscFlags

Flags (see <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined by using a logical OR. For a texture cube-map, set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_TEXTURECUBE</a> flag. Cube-map arrays (that is, <b>ArraySize</b> &gt; 6) require feature level <a href="d3d_feature_level.htm">D3D_FEATURE_LEVEL_10_1</a> or higher.


#### - TextureLayout

A <a href="https://msdn.microsoft.com/E7786550-99FC-4F8E-B93F-C2877C052EC2">D3D11_TEXTURE_LAYOUT</a>-typed value that identifies the layout of the texture.

The TextureLayout parameter selects both the actual layout of the texture in memory and the layout visible to the application while the texture is mapped.  These flags may not be requested without CPU access also requested.

It is illegal to set CPU access flags on default textures without also setting TextureLayout to a value other than D3D11_TEXTURE_LAYOUT_UNDEFINED.  

D3D11_TEXTURE_LAYOUT_ROW_MAJOR may only be used to create non-multisampled, textures with a single subresource (Planar YUV textures are supported).  These textures may only be used as a source and destination of copy operations, and BindFlags must be zero.


D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE may only be used to create non-multisampled, non-depth-stencil textures.  


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/50C5789A-2C8E-49CB-9348-639CF8B971EC">ID3D11Device3::CreateTexture2D1</a>.

In addition to this structure, you can also use the <b>CD3D11_TEXTURE2D_DESC1</b> derived structure, which is defined  in D3D11_3.h and behaves like an inherited class, to help create a texture description.

The device places some size restrictions (must be multiples of a minimum size) for a subsampled, block compressed, or bit-format resource.

The texture size range is determined by the <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> at which you create the device and not the Microsoft Direct3D interface version. For example, if you use Microsoft Direct3D 10 hardware at feature level 10 (<a href="d3d_feature_level.htm">D3D_FEATURE_LEVEL_10_0</a>) and call <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a> to create an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>, you must constrain the maximum texture size to D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION (8192) when you create your 2D texture.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

