---
UID: NF:d3d10.D3D10CalcSubresource
title: D3D10CalcSubresource function (d3d10.h)
description: Calculate a subresource index for a texture.
helpviewer_keywords: ["91f92116-0ae9-0407-3cba-2a8ff2762095","D3D10CalcSubresource","D3D10CalcSubresource function [Direct3D 10]","d3d10/D3D10CalcSubresource","direct3d10.d3d10calcsubresource"]
old-location: direct3d10\d3d10calcsubresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10calcsubresource.htm
ms.date: 12/05/2018
ms.keywords: 91f92116-0ae9-0407-3cba-2a8ff2762095, D3D10CalcSubresource, D3D10CalcSubresource function [Direct3D 10], d3d10/D3D10CalcSubresource, direct3d10.d3d10calcsubresource
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
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10CalcSubresource
 - d3d10/D3D10CalcSubresource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CalcSubresource
---

# D3D10CalcSubresource function


## -description

Calculate a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> index for a texture.

## -parameters

### -param MipSlice [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index into an array of subtextures; 0 indicates the first, most detailed subtexture (or mipmap level).

### -param ArraySlice [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the first texture to use (in an array of textures).

### -param MipLevels [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of mipmap levels (or subtextures) to use.

## -returns

Type: <b>inline UINT</b>

The index which equals <i>MipSlice</i> + (<i>ArraySlice</i> * <i>MipLevels</i>).

## -remarks

A buffer is an unstructured resource and is therefore defined as containing a single subresource. APIs that take buffers do not need a subresource index. A texture on the other hand is highly structured. Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-functions">Resource Functions</a>