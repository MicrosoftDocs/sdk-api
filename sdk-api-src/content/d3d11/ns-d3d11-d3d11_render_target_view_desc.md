---
UID: NS:d3d11.D3D11_RENDER_TARGET_VIEW_DESC
title: D3D11_RENDER_TARGET_VIEW_DESC (d3d11.h)
description: Specifies the subresources from a resource that are accessible using a render-target view.
helpviewer_keywords: ["0571f2fa-1f94-b9a4-ea30-5f99a077c507","D3D11_RENDER_TARGET_VIEW_DESC","D3D11_RENDER_TARGET_VIEW_DESC structure [Direct3D 11]","d3d11/D3D11_RENDER_TARGET_VIEW_DESC","direct3d11.d3d11_render_target_view_desc"]
old-location: direct3d11\d3d11_render_target_view_desc.htm
tech.root: direct3d11
ms.assetid: b154ac98-49ed-4d00-8cb6-5e57680e125c
ms.date: 12/05/2018
ms.keywords: 0571f2fa-1f94-b9a4-ea30-5f99a077c507, D3D11_RENDER_TARGET_VIEW_DESC, D3D11_RENDER_TARGET_VIEW_DESC structure [Direct3D 11], d3d11/D3D11_RENDER_TARGET_VIEW_DESC, direct3d11.d3d11_render_target_view_desc
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
req.typenames: D3D11_RENDER_TARGET_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_RENDER_TARGET_VIEW_DESC
 - d3d11/D3D11_RENDER_TARGET_VIEW_DESC
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
 - D3D11_RENDER_TARGET_VIEW_DESC
---

# D3D11_RENDER_TARGET_VIEW_DESC structure


## -description

Specifies the subresources from a resource that are accessible using a render-target view.

## -struct-fields

### -field Format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The data format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).

### -field ViewDimension

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_rtv_dimension">D3D11_RTV_DIMENSION</a></b>

The resource type (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_rtv_dimension">D3D11_RTV_DIMENSION</a>), which specifies how the render-target resource will be accessed.

### -field Buffer

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_rtv">D3D11_BUFFER_RTV</a></b>

Specifies which buffer elements can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_rtv">D3D11_BUFFER_RTV</a>).

### -field Texture1D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_rtv">D3D11_TEX1D_RTV</a></b>

Specifies the subresources in a 1D texture that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_rtv">D3D11_TEX1D_RTV</a>).

### -field Texture1DArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_rtv">D3D11_TEX1D_ARRAY_RTV</a></b>

Specifies the subresources in a 1D texture array that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_array_rtv">D3D11_TEX1D_ARRAY_RTV</a>).

### -field Texture2D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_rtv">D3D11_TEX2D_RTV</a></b>

Specifies the subresources in a 2D texture that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_rtv">D3D11_TEX2D_RTV</a>).

### -field Texture2DArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_array_rtv">D3D11_TEX2D_ARRAY_RTV</a></b>

Specifies the subresources in a 2D texture array that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2d_array_rtv">D3D11_TEX2D_ARRAY_RTV</a>).

### -field Texture2DMS

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_rtv">D3D11_TEX2DMS_RTV</a></b>

Specifies a single subresource because a multisampled 2D texture only contains one subresource (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_rtv">D3D11_TEX2DMS_RTV</a>).

### -field Texture2DMSArray

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_rtv">D3D11_TEX2DMS_ARRAY_RTV</a></b>

Specifies the subresources in a multisampled 2D texture array that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex2dms_array_rtv">D3D11_TEX2DMS_ARRAY_RTV</a>).

### -field Texture3D

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_rtv">D3D11_TEX3D_RTV</a></b>

Specifies subresources in a 3D texture that can be accessed (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex3d_rtv">D3D11_TEX3D_RTV</a>).

## -remarks

A render-target-view description is passed into <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">ID3D11Device::CreateRenderTargetView</a> to create a render target.

A render-target-view cannot use the following formats:

<ul>
<li>Any typeless format.</li>
<li>DXGI_FORMAT_R32G32B32 if the view will be used to bind a buffer (vertex, index, constant, or stream-output).</li>
</ul>
If the format is set to DXGI_FORMAT_UNKNOWN, then the format of the resource that the view binds to the pipeline will be used.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>