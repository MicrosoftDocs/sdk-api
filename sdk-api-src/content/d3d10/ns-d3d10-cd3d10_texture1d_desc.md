---
UID: NS:d3d10.CD3D10_TEXTURE1D_DESC
title: CD3D10_TEXTURE1D_DESC (d3d10.h)
description: Describes a 1D texture.
helpviewer_keywords: ["3b8edbcf-2f3c-dbad-9241-29cfd861f8cf","CD3D10_TEXTURE1D_DESC","D3D10_TEXTURE1D_DESC","D3D10_TEXTURE1D_DESC structure [Direct3D 10]","d3d10/D3D10_TEXTURE1D_DESC","direct3d10.d3d10_texture1d_desc"]
old-location: direct3d10\d3d10_texture1d_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texture1d_desc.htm
ms.date: 12/05/2018
ms.keywords: 3b8edbcf-2f3c-dbad-9241-29cfd861f8cf, CD3D10_TEXTURE1D_DESC, D3D10_TEXTURE1D_DESC, D3D10_TEXTURE1D_DESC structure [Direct3D 10], d3d10/D3D10_TEXTURE1D_DESC, direct3d10.d3d10_texture1d_desc
f1_keywords:
- d3d10/D3D10_TEXTURE1D_DESC
dev_langs:
- c++
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
- D3D10_TEXTURE1D_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CD3D10_TEXTURE1D_DESC structure


## -description


Describes a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a>.


## -struct-fields




### -field CD3D10_TEXTURE1D_DESC

TBD 


### -field ~CD3D10_TEXTURE1D_DESC

TBD 


### -field operator const D3D10_TEXTURE1D_DESC&

TBD 


### -field D3D10_TEXTURE1D_DESC

 




#### - ArraySize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures in the array. The range is from 1 to D3D10_REQ_TEXTURE1D_ARRAY_AXIS_DIMENSION (512).


#### - BindFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_FLAG</a>) for binding to <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a> stages. The flags can be combined by a logical OR.


#### - CPUAccessFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_FLAG</a>) to specify the types of CPU access allowed. Use 0 if CPU access is not required. These flags can be combined with a logical OR.


#### - Format

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

Texture format (see <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).


#### - MipLevels

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of subtextures (also called mipmap levels). Use 1 for a multisampled texture; or 0 to generate a full set of subtextures.


#### - MiscFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_FLAG</a>) that identify other, less common resource options. Use 0 if none of these flags apply. These flags can be combined with a logical OR.


#### - Usage

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a></b>

Value that identifies how the texture is to be read from and written to. The most common value is D3D10_USAGE-DEFAULT; see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a> for all possible values.


#### - Width

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Texture width (in texels). The range is from 1 to D3D10_REQ_TEXTURE1D_U_DIMENSION (8192).


## -remarks



This structure is used in a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture1d">ID3D10Device::CreateTexture1D</a>. A helpful derived structure CD3D10_TEXTURE1D_DESC is declared in D3D10.h, to help create a texture description.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
 

 

