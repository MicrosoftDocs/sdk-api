---
UID: NF:d3d11.ID3D11Device.CreateTexture3D
title: ID3D11Device::CreateTexture3D (d3d11.h)
description: Create a single 3D texture.
helpviewer_keywords: ["CreateTexture3D","CreateTexture3D method [Direct3D 11]","CreateTexture3D method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateTexture3D method","ID3D11Device.CreateTexture3D","ID3D11Device::CreateTexture3D","d3d11/ID3D11Device::CreateTexture3D","d98ea118-c203-f23f-517e-92225bfe119d","direct3d11.id3d11device_createtexture3d"]
old-location: direct3d11\id3d11device_createtexture3d.htm
tech.root: direct3d11
ms.assetid: 92b31baf-2d64-47fe-bd0d-550f2a65ed9a
ms.date: 12/05/2018
ms.keywords: CreateTexture3D, CreateTexture3D method [Direct3D 11], CreateTexture3D method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateTexture3D method, ID3D11Device.CreateTexture3D, ID3D11Device::CreateTexture3D, d3d11/ID3D11Device::CreateTexture3D, d98ea118-c203-f23f-517e-92225bfe119d, direct3d11.id3d11device_createtexture3d
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreateTexture3D
 - d3d11/ID3D11Device::CreateTexture3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateTexture3D
---

# ID3D11Device::CreateTexture3D


## -description

Create a single <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro">3D texture</a>.

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a> structure that describes a 3D texture resource. To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.

### -param pInitialData [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a> structures that describe subresources for the 3D texture resource. Applications cannot specify <b>NULL</b> for <i>pInitialData</i> when creating IMMUTABLE resources (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a>). If the resource is multisampled, <i>pInitialData</i> must be <b>NULL</b> because multisampled resources cannot be initialized with data when they are created.

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the resource is undefined. In this case, you need to write the resource content some other way before the resource is read.

You can determine the size of this array from the value in the <b>MipLevels</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a> structure to which <i>pDesc</i> points. Arrays of 3D volume textures are not supported.

For more information about this array size, see Remarks.

### -param ppTexture3D [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture3d">ID3D11Texture3D</a>**</b>

A pointer to a buffer that receives a pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture3d">ID3D11Texture3D</a> interface for the created texture. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for failing error codes.

## -remarks

<b>CreateTexture3D</b> creates a 3D texture resource, which can contain a number of 3D subresources. The number of textures is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more subresources. To load data into the texture, applications can supply the data initially as an array of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a> structures pointed to by <i>pInitialData</i>, or they can use one of the D3DX texture functions such as <a href="/windows/desktop/direct3d11/d3dx11createtexturefromfile">D3DX11CreateTextureFromFile</a>.

Each element of <i>pInitialData</i> provides all of the slices that are defined for a given miplevel. For example, for a 32 x 32 x 4 volume texture with a full mipmap chain, the array has the following 6 elements:

<ul>
<li>pInitialData[0] = 32x32 with 4 slices</li>
<li>pInitialData[1] = 16x16 with 2 slices</li>
<li>pInitialData[2] = 8x8 with 1 slice</li>
<li>pInitialData[3] = 4x4
with 1 slice</li>
<li>pInitialData[4] = 2x2
with 1 slice</li>
<li>pInitialData[5] = 1x1
with 1 slice</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>