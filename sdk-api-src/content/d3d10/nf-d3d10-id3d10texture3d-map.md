---
UID: NF:d3d10.ID3D10Texture3D.Map
title: ID3D10Texture3D::Map (d3d10.h)
description: Get a pointer to the data contained in a subresource, and deny GPU access to that subresource. (ID3D10Texture3D.Map)
helpviewer_keywords: ["0a753acc-a6b4-f192-8a52-1069da27bbff","ID3D10Texture3D interface [Direct3D 10]","Map method","ID3D10Texture3D.Map","ID3D10Texture3D::Map","Map","Map method [Direct3D 10]","Map method [Direct3D 10]","ID3D10Texture3D interface","d3d10/ID3D10Texture3D::Map","direct3d10.id3d10texture3d_map"]
old-location: direct3d10\id3d10texture3d_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d_map.htm
ms.date: 12/05/2018
ms.keywords: 0a753acc-a6b4-f192-8a52-1069da27bbff, ID3D10Texture3D interface [Direct3D 10],Map method, ID3D10Texture3D.Map, ID3D10Texture3D::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Texture3D interface, d3d10/ID3D10Texture3D::Map, direct3d10.id3d10texture3d_map
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
 - ID3D10Texture3D::Map
 - d3d10/ID3D10Texture3D::Map
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
 - ID3D10Texture3D.Map
---

# ID3D10Texture3D::Map


## -description

Get a pointer to the data contained in a subresource, and deny GPU access to that subresource.

## -parameters

### -param Subresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index number of the subresource. See <a href="/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.

### -param MapType [in]

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a></b>

Specifies the CPU's read and write permissions for a resource. For possible values, see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a>.

### -param MapFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map_flag">Flag</a> that specifies what the CPU should do when the GPU is busy. This flag is optional.

### -param pMappedTex3D [out]

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_mapped_texture3d">D3D10_MAPPED_TEXTURE3D</a>*</b>

Pointer to a structure (<a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_mapped_texture3d">D3D10_MAPPED_TEXTURE3D</a>) that is filled in by the function and contains a pointer to the resource data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns S_OK. All of the Map methods have identical return values and operating restrictions. These are listed in the remarks section of <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-map">ID3D10Texture1D::Map</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10texture3d">ID3D10Texture3D Interface</a>
