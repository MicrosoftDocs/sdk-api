---
UID: NS:d3d12.D3D12_UNORDERED_ACCESS_VIEW_DESC
title: D3D12_UNORDERED_ACCESS_VIEW_DESC (d3d12.h)
description: Describes the subresources from a resource that are accessible by using an unordered-access view.
helpviewer_keywords: ["D3D12_UNORDERED_ACCESS_VIEW_DESC","D3D12_UNORDERED_ACCESS_VIEW_DESC structure","d3d12/D3D12_UNORDERED_ACCESS_VIEW_DESC","direct3d12.d3d12_unordered_access_view_desc"]
old-location: direct3d12\d3d12_unordered_access_view_desc.htm
tech.root: direct3d12
ms.assetid: 0C3A31FE-625D-4CB3-87FD-D2C33D008DD4
ms.date: 12/05/2018
ms.keywords: D3D12_UNORDERED_ACCESS_VIEW_DESC, D3D12_UNORDERED_ACCESS_VIEW_DESC structure, d3d12/D3D12_UNORDERED_ACCESS_VIEW_DESC, direct3d12.d3d12_unordered_access_view_desc
req.header: d3d12.h
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
req.typenames: D3D12_UNORDERED_ACCESS_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_UNORDERED_ACCESS_VIEW_DESC
 - d3d12/D3D12_UNORDERED_ACCESS_VIEW_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_UNORDERED_ACCESS_VIEW_DESC
---

# D3D12_UNORDERED_ACCESS_VIEW_DESC structure


## -description

Describes the subresources from a resource that are accessible by using an unordered-access view.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the viewing format.

### -field ViewDimension

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension">D3D12_UAV_DIMENSION</a>-typed value that specifies the resource type of the view. This type specifies how the resource will be accessed. This member also determines which _UAV to use in the union below.

### -field Buffer

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav">D3D12_BUFFER_UAV</a> structure that specifies which buffer elements can be accessed.

### -field Texture1D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav">D3D12_TEX1D_UAV</a> structure that specifies the subresources in a 1D texture that can be accessed.

### -field Texture1DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav">D3D12_TEX1D_ARRAY_UAV</a> structure that specifies the subresources in a 1D texture array that can be accessed.

### -field Texture2D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav">D3D12_TEX2D_UAV</a> structure that specifies the subresources in a 2D texture that can be accessed.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav">D3D12_TEX2D_ARRAY_UAV</a> structure that specifies the subresources in a 2D texture array that can be accessed.

### -field Texture3D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav">D3D12_TEX3D_UAV</a> structure that specifies subresources in a 3D texture that can be accessed.

## -remarks

Pass an unordered-access-view description into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview">ID3D12Device::CreateUnorderedAccessView</a> to create a view.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>