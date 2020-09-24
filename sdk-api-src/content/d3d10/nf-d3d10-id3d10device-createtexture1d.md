---
UID: NF:d3d10.ID3D10Device.CreateTexture1D
title: ID3D10Device::CreateTexture1D (d3d10.h)
description: Create an array of 1D textures (see Texture1D).
helpviewer_keywords: ["0ea074c9-00a2-6fa9-2aad-24c30631a07a","CreateTexture1D","CreateTexture1D method [Direct3D 10]","CreateTexture1D method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateTexture1D method","ID3D10Device.CreateTexture1D","ID3D10Device::CreateTexture1D","d3d10/ID3D10Device::CreateTexture1D","direct3d10.id3d10device_createtexture1d"]
old-location: direct3d10\id3d10device_createtexture1d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createtexture1d.htm
ms.date: 12/05/2018
ms.keywords: 0ea074c9-00a2-6fa9-2aad-24c30631a07a, CreateTexture1D, CreateTexture1D method [Direct3D 10], CreateTexture1D method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateTexture1D method, ID3D10Device.CreateTexture1D, ID3D10Device::CreateTexture1D, d3d10/ID3D10Device::CreateTexture1D, direct3d10.id3d10device_createtexture1d
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CreateTexture1D
 - d3d10/ID3D10Device::CreateTexture1D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateTexture1D
---

# ID3D10Device::CreateTexture1D


## -description

Create an array of 1D textures (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Texture1D</a>).

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture1d_desc">D3D10_TEXTURE1D_DESC</a>*</b>

Pointer to a 1D texture description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture1d_desc">D3D10_TEXTURE1D_DESC</a>). To create a typeless resource that can be interpreted at runtime into different, compatible formats, specify a typeless format in the texture description. To generate mipmap levels automatically, set the number of mipmap levels to 0.

### -param pInitialData [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_subresource_data">D3D10_SUBRESOURCE_DATA</a>*</b>

Pointer to an array of <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> descriptions (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_subresource_data">D3D10_SUBRESOURCE_DATA</a>); one for each subresource (ordered by texture array index). Applications may not specify <b>NULL</b> for pInitialData when creating IMMUTABLE resources (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a>). If the resource is multisampled, pInitialData must be <b>NULL</b> because multisampled resources cannot be initialized with data when they are created.

### -param ppTexture1D [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10texture1d">ID3D10Texture1D</a>**</b>

Address of a pointer to the created texture (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10texture1d">ID3D10Texture1D Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a> for failing error codes.

## -remarks

CreateTexture1D creates a 1D texture resource, which contains an array of 1D textures. The number of textures is specified in the texture description. All textures in a resource must have the same format, size, and number of mipmap levels.

All resources are made up of one or more <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresources</a>. To load data into the texture, applications may supply the data initially as part of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_subresource_data">D3D10_SUBRESOURCE_DATA</a> structure pointed to by pInitialData, or it may use one of the <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3dx10-functions-texturing">Texturing Functions</a> supplied by the SDK.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>