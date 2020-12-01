---
UID: NS:d3d12.D3D12_RENDER_TARGET_VIEW_DESC
title: D3D12_RENDER_TARGET_VIEW_DESC (d3d12.h)
description: Describes the subresources from a resource that are accessible by using a render-target view.
helpviewer_keywords: ["D3D12_RENDER_TARGET_VIEW_DESC","D3D12_RENDER_TARGET_VIEW_DESC structure","d3d12/D3D12_RENDER_TARGET_VIEW_DESC","direct3d12.d3d12_render_target_view_desc"]
old-location: direct3d12\d3d12_render_target_view_desc.htm
tech.root: direct3d12
ms.assetid: D8602EB9-70EB-4A4E-8D8D-A2016335AAC6
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_TARGET_VIEW_DESC, D3D12_RENDER_TARGET_VIEW_DESC structure, d3d12/D3D12_RENDER_TARGET_VIEW_DESC, direct3d12.d3d12_render_target_view_desc
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
req.typenames: D3D12_RENDER_TARGET_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_TARGET_VIEW_DESC
 - d3d12/D3D12_RENDER_TARGET_VIEW_DESC
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
 - D3D12_RENDER_TARGET_VIEW_DESC
---

# D3D12_RENDER_TARGET_VIEW_DESC structure


## -description

Describes the subresources from a resource that are accessible by using a render-target view.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the viewing format.

### -field ViewDimension

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension">D3D12_RTV_DIMENSION</a>-typed value that specifies how the render-target resource will be accessed. This type specifies how the resource will be accessed. This member also determines which _RTV to use in the following union.

### -field Buffer

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv">D3D12_BUFFER_RTV</a> structure that specifies which buffer elements can be accessed.

### -field Texture1D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv">D3D12_TEX1D_RTV</a> structure that specifies the subresources in a 1D texture that can be accessed.

### -field Texture1DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv">D3D12_TEX1D_ARRAY_RTV</a> structure that specifies the subresources in a 1D texture array that can be accessed.

### -field Texture2D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv">D3D12_TEX2D_RTV</a> structure that specifies the subresources in a 2D texture that can be accessed.

### -field Texture2DArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv">D3D12_TEX2D_ARRAY_RTV</a> structure that specifies the subresources in a 2D texture array that can be accessed.

### -field Texture2DMS

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv">D3D12_TEX2DMS_RTV</a> structure that specifies a single subresource because a multisampled 2D texture only contains one subresource.

### -field Texture2DMSArray

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv">D3D12_TEX2DMS_ARRAY_RTV</a> structure that specifies the subresources in a multisampled 2D texture array that can be accessed.

### -field Texture3D

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv">D3D12_TEX3D_RTV</a> structure that specifies subresources in a 3D texture that can be accessed.

## -remarks

Pass a render-target-view description into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview">ID3D12Device::CreateRenderTargetView</a> to create a render-target view.

A render-target view can't use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>