---
UID: NS:d3d11.D3D11_TEX3D_UAV
title: D3D11_TEX3D_UAV (d3d11.h)
description: Describes a unordered-access 3D texture resource. (D3D11_TEX3D_UAV)
helpviewer_keywords: ["3576e4ac-e8c6-2390-6df1-4597956a1b86","D3D11_TEX3D_UAV","D3D11_TEX3D_UAV structure [Direct3D 11]","d3d11/D3D11_TEX3D_UAV","direct3d11.d3d11_tex3d_uav"]
old-location: direct3d11\d3d11_tex3d_uav.htm
tech.root: direct3d11
ms.assetid: 5668c7be-73d1-4407-ace6-8970d723fc44
ms.date: 12/05/2018
ms.keywords: 3576e4ac-e8c6-2390-6df1-4597956a1b86, D3D11_TEX3D_UAV, D3D11_TEX3D_UAV structure [Direct3D 11], d3d11/D3D11_TEX3D_UAV, direct3d11.d3d11_tex3d_uav
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_TEX3D_UAV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX3D_UAV
 - d3d11/D3D11_TEX3D_UAV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX3D_UAV
---

# D3D11_TEX3D_UAV structure


## -description

Describes a unordered-access 3D texture resource.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The mipmap slice index.

### -field FirstWSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the first depth slice to be accessed.

### -field WSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of depth slices.

## -remarks

This structure is used by a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
