---
UID: NS:d3d10.D3D10_TEXTURE3D_DESC
title: D3D10_TEXTURE3D_DESC
author: windows-sdk-content
description: Describes a 3D texture.
old-location: direct3d10\d3d10_texture3d_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texture3d_desc.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CD3D10_TEXTURE3D_DESC, D3D10_TEXTURE3D_DESC, D3D10_TEXTURE3D_DESC structure [Direct3D 10], abbd74e0-643f-c06c-689d-08361a07731d, d3d10/D3D10_TEXTURE3D_DESC, direct3d10.d3d10_texture3d_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
req.typenames: D3D10_TEXTURE3D_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEXTURE3D_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEXTURE3D_DESC structure


## -description


Describes a <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">3D texture</a>.


## -struct-fields




#### - Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture width (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). For more information about restrictions, see Remarks.


#### - Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture height (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048). For more information about restrictions, see Remarks.


#### - Depth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Texture depth (in texels). The range is from 1 to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION (2048).


#### - MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of subtextures (also called mipmap levels). Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


#### - Format

Type: <b><a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Texture format (see <a href="https://msdn.microsoft.com/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>).


#### - Usage

Type: <b><a href="https://msdn.microsoft.com/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a></b>

Value that identifies how the texture is to be read from and written to. The most common value is D3D10_USAGE-DEFAULT; see <a href="https://msdn.microsoft.com/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a> for all possible values.


#### - BindFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/library/Bb204891(v=VS.85).aspx">D3D10_BIND_FLAG</a>) for binding to <a href="https://msdn.microsoft.com/library/Bb205123(v=VS.85).aspx">pipeline</a> stages. The flags can be combined by a logical OR.


#### - CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/library/Bb204908(v=VS.85).aspx">D3D10_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.


#### - MiscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/library/Bb172412(v=VS.85).aspx">D3D10_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a logical OR.


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/library/Bb173561(v=VS.85).aspx">ID3D10Device::CreateTexture3D</a>. A helpful derived structure CD3D10_TEXTURE3D_DESC is declared in D3D10.h, to help create a texture description.

The device restricts the size of subsampled, block compressed (see <a href="https://msdn.microsoft.com/library/Bb694531(v=VS.85).aspx">Block Compression (Direct3D 10)</a>), and bit format resources to be multiples of sizes specific to each format.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

