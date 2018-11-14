---
UID: NS:d3d10.D3D10_TEXTURE2D_DESC
title: D3D10_TEXTURE2D_DESC
author: windows-sdk-content
description: Describes a 2D texture.
old-location: direct3d10\d3d10_texture2d_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texture2d_desc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 53736d47-a636-d91b-ae36-38e32953d08c, CD3D10_TEXTURE2D_DESC, D3D10_TEXTURE2D_DESC, D3D10_TEXTURE2D_DESC structure [Direct3D 10], d3d10/D3D10_TEXTURE2D_DESC, direct3d10.d3d10_texture2d_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEXTURE2D_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_TEXTURE2D_DESC
req.redist: 
---

# D3D10_TEXTURE2D_DESC structure


## -description


Describes a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a>.


## -struct-fields




#### - Width

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Texture width (in texels). The range is from 1 to D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION (8192). For a texture cube-map, the range is from 1 to D3D10_REQ_TEXTURECUBE_DIMENSION (8192). For more information about restrictions, see Remarks.


#### - Height

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Texture height (in texels). The range is from 1 to D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION (8192). For a texture cube-map, the range is from 1 to D3D10_REQ_TEXTURECUBE_DIMENSION (8192). For more information about restrictions, see Remarks.


#### - MipLevels

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of subtextures (also called mipmap levels). Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


#### - ArraySize

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of textures in the texture array. The range is from 1 to D3D10_REQ_TEXTURE2D_ARRAY_AXIS_DIMENSION (512). For a texture cube-map, this value is a multiple of 6 (that is, 6 * the value in the <b>NumCubes</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb694536(v=VS.85).aspx">D3D10_TEXCUBE_ARRAY_SRV1</a>), and the range is from 6 to D3D10_REQ_TEXTURECUBE_DIMENSION.


#### - Format

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a></b>

Texture format (see <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>).


#### - SampleDesc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a></b>

Structure that specifies multisampling parameters for the texture. See <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a>.


#### - Usage

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a></b>

Value that identifies how the texture is to be read from and written to. The most common value is D3D10_USAGE-DEFAULT; see <a href="https://msdn.microsoft.com/en-us/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a> for all possible values.


#### - BindFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_FLAG</a>) for binding to <a href="https://msdn.microsoft.com/en-us/library/Bb205123(v=VS.85).aspx">pipeline</a> stages. The flags can be combined by a logical OR.


#### - CPUAccessFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204908(v=VS.85).aspx">D3D10_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.


#### - MiscFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb172412(v=VS.85).aspx">D3D10_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a logical OR. For a texture cube-map, set the <a href="https://msdn.microsoft.com/en-us/library/Bb172412(v=VS.85).aspx">D3D10_RESOURCE_MISC_TEXTURECUBE</a> flag. Cube-map arrays (that is, <b>ArraySize</b> &gt; 6) require feature level <a href="https://msdn.microsoft.com/en-us/library/Ff476329(v=VS.85).aspx">D3D_FEATURE_LEVEL_10_1</a>.


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/en-us/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a>. A helpful derived structure CD3D10_TEXTURE2D_DESC is declared in D3D10.h, to help create a texture description.

The device places some size restrictions (must be multiples of a minimum size) for a subsampled, <a href="https://msdn.microsoft.com/en-us/library/Bb694531(v=VS.85).aspx">block compressed</a>, or bit-format resource.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

