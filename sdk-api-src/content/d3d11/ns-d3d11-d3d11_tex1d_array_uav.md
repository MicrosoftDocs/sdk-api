---
UID: NS:d3d11.D3D11_TEX1D_ARRAY_UAV
title: D3D11_TEX1D_ARRAY_UAV (d3d11.h)
description: Describes an array of unordered-access 1D texture resources.
old-location: direct3d11\d3d11_tex1d_array_uav.htm
tech.root: direct3d11
ms.assetid: 8a637d5f-b9cb-486b-8f43-4925cee9ccf7
ms.date: 12/05/2018
ms.keywords: 996cd2a4-b335-16f3-2420-8b9fadb414b0, D3D11_TEX1D_ARRAY_UAV, D3D11_TEX1D_ARRAY_UAV structure [Direct3D 11], d3d11/D3D11_TEX1D_ARRAY_UAV, direct3d11.d3d11_tex1d_array_uav
ms.topic: struct
f1_keywords:
- d3d11/D3D11_TEX1D_ARRAY_UAV
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D11.h
api_name:
- D3D11_TEX1D_ARRAY_UAV
targetos: Windows
req.typenames: D3D11_TEX1D_ARRAY_UAV
req.redist: 
ms.custom: 19H1
---

# D3D11_TEX1D_ARRAY_UAV structure


## -description


Describes an array of unordered-access 1D texture resources.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The mipmap slice index.


### -field FirstArraySlice

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the first array slice to be accessed.


### -field ArraySize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of slices in the array.


## -remarks



This structure is used by a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
 

 

