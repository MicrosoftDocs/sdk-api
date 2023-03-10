---
UID: NS:d3d11_3.D3D11_UNORDERED_ACCESS_VIEW_DESC1
title: D3D11_UNORDERED_ACCESS_VIEW_DESC1 (d3d11_3.h)
description: Describes the subresources from a resource that are accessible using an unordered-access view. (D3D11_UNORDERED_ACCESS_VIEW_DESC1)
helpviewer_keywords: ["CD3D11_UNORDERED_ACCESS_VIEW_DESC1","D3D11_UNORDERED_ACCESS_VIEW_DESC1","D3D11_UNORDERED_ACCESS_VIEW_DESC1 structure [Direct3D 11]","d3d11_3/D3D11_UNORDERED_ACCESS_VIEW_DESC1","direct3d11.d3d11_unordered_access_view_desc1"]
old-location: direct3d11\d3d11_unordered_access_view_desc1.htm
tech.root: direct3d11
ms.assetid: 833B4B8A-5702-4C17-AFD2-DFDF69354DDD
ms.date: 12/05/2018
ms.keywords: CD3D11_UNORDERED_ACCESS_VIEW_DESC1, D3D11_UNORDERED_ACCESS_VIEW_DESC1, D3D11_UNORDERED_ACCESS_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_UNORDERED_ACCESS_VIEW_DESC1, direct3d11.d3d11_unordered_access_view_desc1
req.header: d3d11_3.h
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
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_UNORDERED_ACCESS_VIEW_DESC1
 - d3d11_3/D3D11_UNORDERED_ACCESS_VIEW_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_UNORDERED_ACCESS_VIEW_DESC1
---

## -description

Describes the subresources from a resource that are accessible using an unordered-access view.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the data format.

### -field ViewDimension

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_uav_dimension">D3D11_UAV_DIMENSION</a>-typed value that  specifies the resource type of the view. This type is the same as the resource type of the underlying resource. This member also determines which _UAV to use in the union below.

### -field Buffer

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_uav">D3D11_BUFFER_UAV</a> structure that specifies which buffer elements can be accessed.

### -field Texture1D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_uav">D3D11_TEX1D_UAV</a> structure that specifies the subresources in a 1D texture that can be accessed.

### -field Texture1DArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_uav">D3D11_TEX1D_ARRAY_UAV</a> structure that specifies the subresources in a 1D texture array that can be accessed.

### -field Texture2D

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_uav1">D3D11_TEX2D_UAV1</a> structure that specifies the subresources in a 2D texture that can be accessed.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_array_uav1">D3D11_TEX2D_ARRAY_UAV1</a> structure that specifies the subresources in a 2D texture array that can be accessed.

### -field Texture3D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_uav">D3D11_TEX3D_UAV</a> structure that specifies subresources in a 3D texture that can be accessed.

## -remarks

An unordered-access-view description is passed into <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createunorderedaccessview1">ID3D11Device3::CreateUnorderedAccessView1</a> to create a view.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
