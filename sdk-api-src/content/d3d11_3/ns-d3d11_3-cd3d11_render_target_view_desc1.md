---
UID: NS:d3d11_3.CD3D11_RENDER_TARGET_VIEW_DESC1
title: CD3D11_RENDER_TARGET_VIEW_DESC1 (d3d11_3.h)
description: Describes the subresources from a resource that are accessible using a render-target view.D
helpviewer_keywords: ["CD3D11_RENDER_TARGET_VIEW_DESC1","D3D11_RENDER_TARGET_VIEW_DESC1","D3D11_RENDER_TARGET_VIEW_DESC1 structure [Direct3D 11]","d3d11_3/D3D11_RENDER_TARGET_VIEW_DESC1","direct3d11.d3d11_render_target_view_desc1"]
old-location: direct3d11\d3d11_render_target_view_desc1.htm
tech.root: direct3d11
ms.assetid: D87F06B4-7574-4BBD-A481-653CA35B8FB2
ms.date: 12/05/2018
ms.keywords: CD3D11_RENDER_TARGET_VIEW_DESC1, D3D11_RENDER_TARGET_VIEW_DESC1, D3D11_RENDER_TARGET_VIEW_DESC1 structure [Direct3D 11], d3d11_3/D3D11_RENDER_TARGET_VIEW_DESC1, direct3d11.d3d11_render_target_view_desc1
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_RENDER_TARGET_VIEW_DESC1
 - d3d11_3/CD3D11_RENDER_TARGET_VIEW_DESC1
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
 - D3D11_RENDER_TARGET_VIEW_DESC1
---

# CD3D11_RENDER_TARGET_VIEW_DESC1 structure


## -description

Describes the subresources from a resource that are accessible using a render-target view.

## -struct-fields

### -field CD3D11_RENDER_TARGET_VIEW_DESC1

TBD

### -field ~CD3D11_RENDER_TARGET_VIEW_DESC1

TBD

### -field operator const D3D11_RENDER_TARGET_VIEW_DESC1&

TBD

### -field D3D11_RENDER_TARGET_VIEW_DESC1

 




#### - Buffer

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_rtv">D3D11_BUFFER_RTV</a> structure that specifies which buffer elements can be accessed.


#### - Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the data format.




#### - Texture1D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_rtv">D3D11_TEX1D_RTV</a> structure that specifies the subresources in a 1D texture that can be accessed.


#### - Texture1DArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_rtv">D3D11_TEX1D_ARRAY_RTV</a> structure that specifies the subresources in a 1D texture array that can be accessed.


#### - Texture2D

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_rtv1">D3D11_TEX2D_RTV1</a> structure that specifies the subresources in a 2D texture that can be accessed.


#### - Texture2DArray

A <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1">D3D11_TEX2D_ARRAY_RTV1</a> structure that specifies the subresources in a 2D texture array that can be accessed.


#### - Texture2DMS

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_rtv">D3D11_TEX2DMS_RTV</a> structure that specifies a single subresource because a multisampled 2D texture only contains one subresource.


#### - Texture2DMSArray

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_rtv">D3D11_TEX2DMS_ARRAY_RTV</a> structure that specifies the subresources in a multisampled 2D texture array that can be accessed.


#### - Texture3D

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_rtv">D3D11_TEX3D_RTV</a> structure that specifies subresources in a 3D texture that can be accessed.


#### - ViewDimension

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_rtv_dimension">D3D11_RTV_DIMENSION</a>-typed value that specifies the resource type and how the render-target resource will be accessed.

## -remarks

A render-target-view description is passed into <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createrendertargetview1">ID3D11Device3::CreateRenderTargetView1</a> to create a render target.

A render-target-view can't use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
