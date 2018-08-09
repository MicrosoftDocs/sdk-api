---
UID: NS:d3d11.D3D11_TEXTURE3D_DESC
title: D3D11_TEXTURE3D_DESC
author: windows-sdk-content
description: Describes a 3D texture.
old-location: direct3d11\d3d11_texture3d_desc.htm
old-project: direct3d11
ms.assetid: b3fd4280-c967-4eed-8a10-97f0c7ef56ac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 64540f29-b4c0-93ff-f17c-15c6a0d7da4b, D3D11_TEXTURE3D_DESC, D3D11_TEXTURE3D_DESC structure [Direct3D 11], d3d11/D3D11_TEXTURE3D_DESC, direct3d11.d3d11_texture3d_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_TEXTURE3D_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEXTURE3D_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEXTURE3D_DESC structure


## -description


Describes a 3D texture.


## -struct-fields




### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture width (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture height (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


### -field Depth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture depth (in texels). The  range is from 1 to D3D11_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). However, the range is actually constrained by the <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a> at which you create the rendering device. For more information about restrictions, see Remarks.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of mipmap levels in the texture. See the remarks in <a href="https://msdn.microsoft.com/255e97ac-e978-4a70-a908-f4537337dfeb">D3D11_TEX1D_SRV</a>. Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


### -field Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Texture format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>).


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a></b>

Value that identifies how the texture is to be read from and written to. The most common value is D3D11_USAGE_DEFAULT; see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a> for all possible values.


### -field BindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_FLAG</a>) for binding to pipeline stages. The flags can be combined by a logical OR.


### -field CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.


### -field MiscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a logical OR.


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/92b31baf-2d64-47fe-bd0d-550f2a65ed9a">ID3D11Device::CreateTexture3D</a>.

In addition to this structure, you can also use the <a href="https://msdn.microsoft.com/3C2AE448-2EB1-445C-9885-449E02D79EC3">CD3D11_TEXTURE3D_DESC</a> derived structure, which is defined  in D3D11.h and behaves like an inherited class, to help create a texture description.

The device restricts the size of subsampled, block compressed, and bit format resources to be multiples of sizes specific to each format.

The texture size range is determined by the <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a> at which you create the device and not the Microsoft Direct3D interface version. For example, if you use Microsoft Direct3D 10 hardware at feature level 10 (<a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL_10_0</a>) and call <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a> to create an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>, you must constrain the maximum texture size to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048) when you create your 3D texture.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

