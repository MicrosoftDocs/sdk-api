---
UID: NF:d3d11_3.ID3D11Device3.CreateTexture2D1
title: ID3D11Device3::CreateTexture2D1 (d3d11_3.h)
description: Creates a 2D texture.
helpviewer_keywords: ["CreateTexture2D1","CreateTexture2D1 method [Direct3D 11]","CreateTexture2D1 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","CreateTexture2D1 method","ID3D11Device3.CreateTexture2D1","ID3D11Device3::CreateTexture2D1","d3d11_3/ID3D11Device3::CreateTexture2D1","direct3d11.id3d11device3_createtexture2d1"]
old-location: direct3d11\id3d11device3_createtexture2d1.htm
tech.root: direct3d11
ms.assetid: 50C5789A-2C8E-49CB-9348-639CF8B971EC
ms.date: 02/12/2024
ms.keywords: CreateTexture2D1, CreateTexture2D1 method [Direct3D 11], CreateTexture2D1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateTexture2D1 method, ID3D11Device3.CreateTexture2D1, ID3D11Device3::CreateTexture2D1, d3d11_3/ID3D11Device3::CreateTexture2D1, direct3d11.id3d11device3_createtexture2d1
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11Device3::CreateTexture2D1
 - d3d11_3/ID3D11Device3::CreateTexture2D1
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
 - ID3D11Device3.CreateTexture2D1
---

## -description

Creates a <a href="/windows/win32/direct3d11/overviews-direct3d-11-resources-textures-intro">2D texture</a>.

## -parameters

### -param pDesc1 [in]

Type: <b>const <a href="/windows/win32/api/d3d11_3/ns-d3d11_3-d3d11_texture2d_desc1">D3D11_TEXTURE2D_DESC1</a>*</b>

A pointer to a <a href="/windows/win32/api/d3d11_3/ns-d3d11_3-d3d11_texture2d_desc1">D3D11_TEXTURE2D_DESC1</a> structure that describes a 2D texture resource. To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.

### -param pInitialData [in, optional]

Type: <b>const <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a>*</b>

 A pointer to an array of <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a> structures that describe subresources for the 2D texture resource. Applications can't specify <b>NULL</b> for <i>pInitialData</i> when creating IMMUTABLE resources (see <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a>). If the resource is multisampled, <i>pInitialData</i> must be <b>NULL</b> because multisampled resources can't be initialized with data when they're created.

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the resource is undefined. In this case, you need to write the resource content some other way before the resource is read.

You can determine the size of this array from values in the <b>MipLevels</b> and <b>ArraySize</b> members of the <b>D3D11_TEXTURE2D_DESC1</b> structure to which <i>pDesc1</i> points by using the following calculation:

MipLevels * ArraySize

For more info about this array size, see Remarks.

### -param ppTexture2D [out, optional]

Type: <b><a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11texture2d1">ID3D11Texture2D1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11texture2d1">ID3D11Texture2D1</a> interface for the created texture. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return code is <b>S_OK</b>. See <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for failing error codes.

## -remarks

<b>CreateTexture2D1</b> creates a 2D texture resource, which can contain a number of 2D subresources. The number of subresources is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more subresources. To load data into the texture, applications can supply the data initially as an array of <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a> structures pointed to by <i>pInitialData</i>, or they can use one of the D3DX texture functions such as <a href="/windows/win32/direct3d11/d3dx11createtexturefromfile">D3DX11CreateTextureFromFile</a>.

For a 32 x 32 texture with a full mipmap chain, the <i>pInitialData</i> array has the following 6 elements:


<ul>
<li>pInitialData[0] = 32x32</li>
<li>pInitialData[1] = 16x16</li>
<li>pInitialData[2] = 8x8</li>
<li>pInitialData[3] = 4x4
</li>
<li>pInitialData[4] = 2x2
</li>
<li>pInitialData[5] = 1x1
</li>
</ul>

## -see-also

<a href="/windows/win32/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>
