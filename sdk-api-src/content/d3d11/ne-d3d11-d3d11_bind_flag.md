---
UID: NE:d3d11.D3D11_BIND_FLAG
title: D3D11_BIND_FLAG (d3d11.h)
description: Identifies how to bind a resource to the pipeline.
helpviewer_keywords: ["D3D11_BIND_CONSTANT_BUFFER","D3D11_BIND_DECODER","D3D11_BIND_DEPTH_STENCIL","D3D11_BIND_FLAG","D3D11_BIND_FLAG enumeration [Direct3D 11]","D3D11_BIND_INDEX_BUFFER","D3D11_BIND_RENDER_TARGET","D3D11_BIND_SHADER_RESOURCE","D3D11_BIND_STREAM_OUTPUT","D3D11_BIND_UNORDERED_ACCESS","D3D11_BIND_VERTEX_BUFFER","D3D11_BIND_VIDEO_ENCODER","d3d11/D3D11_BIND_CONSTANT_BUFFER","d3d11/D3D11_BIND_DECODER","d3d11/D3D11_BIND_DEPTH_STENCIL","d3d11/D3D11_BIND_FLAG","d3d11/D3D11_BIND_INDEX_BUFFER","d3d11/D3D11_BIND_RENDER_TARGET","d3d11/D3D11_BIND_SHADER_RESOURCE","d3d11/D3D11_BIND_STREAM_OUTPUT","d3d11/D3D11_BIND_UNORDERED_ACCESS","d3d11/D3D11_BIND_VERTEX_BUFFER","d3d11/D3D11_BIND_VIDEO_ENCODER","direct3d11.d3d11_bind_flag","f5054b36-4a79-15b3-51ed-9c008399e353"]
old-location: direct3d11\d3d11_bind_flag.htm
tech.root: direct3d11
ms.assetid: 4ffa1714-bd85-4d5a-930d-20526f46e4b9
ms.date: 12/05/2018
ms.keywords: D3D11_BIND_CONSTANT_BUFFER, D3D11_BIND_DECODER, D3D11_BIND_DEPTH_STENCIL, D3D11_BIND_FLAG, D3D11_BIND_FLAG enumeration [Direct3D 11], D3D11_BIND_INDEX_BUFFER, D3D11_BIND_RENDER_TARGET, D3D11_BIND_SHADER_RESOURCE, D3D11_BIND_STREAM_OUTPUT, D3D11_BIND_UNORDERED_ACCESS, D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_VIDEO_ENCODER, d3d11/D3D11_BIND_CONSTANT_BUFFER, d3d11/D3D11_BIND_DECODER, d3d11/D3D11_BIND_DEPTH_STENCIL, d3d11/D3D11_BIND_FLAG, d3d11/D3D11_BIND_INDEX_BUFFER, d3d11/D3D11_BIND_RENDER_TARGET, d3d11/D3D11_BIND_SHADER_RESOURCE, d3d11/D3D11_BIND_STREAM_OUTPUT, d3d11/D3D11_BIND_UNORDERED_ACCESS, d3d11/D3D11_BIND_VERTEX_BUFFER, d3d11/D3D11_BIND_VIDEO_ENCODER, direct3d11.d3d11_bind_flag, f5054b36-4a79-15b3-51ed-9c008399e353
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
req.typenames: D3D11_BIND_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BIND_FLAG
 - d3d11/D3D11_BIND_FLAG
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
 - D3D11_BIND_FLAG
---

# D3D11_BIND_FLAG enumeration


## -description

Identifies how to bind a resource to the pipeline.

## -enum-fields

### -field D3D11_BIND_VERTEX_BUFFER:0x1L

Bind a buffer as a vertex buffer to the input-assembler stage.

### -field D3D11_BIND_INDEX_BUFFER:0x2L

Bind a buffer as an index buffer to the input-assembler stage.

### -field D3D11_BIND_CONSTANT_BUFFER:0x4L

Bind a buffer as a constant buffer to a shader stage; this flag may NOT be combined with any other bind flag.

### -field D3D11_BIND_SHADER_RESOURCE:0x8L

Bind a buffer or texture to a shader stage; this flag cannot be used with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a> flag.

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.</div>
<div> </div>

### -field D3D11_BIND_STREAM_OUTPUT:0x10L

Bind an output buffer for the stream-output stage.

### -field D3D11_BIND_RENDER_TARGET:0x20L

Bind a texture as a render target for the output-merger stage.

### -field D3D11_BIND_DEPTH_STENCIL:0x40L

Bind a texture as a depth-stencil target for the output-merger stage.

### -field D3D11_BIND_UNORDERED_ACCESS:0x80L

Bind an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource.

### -field D3D11_BIND_DECODER:0x200L

Set this flag to indicate that a  <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro">2D texture</a> is used to receive output from the decoder API. The common way to create resources for a decoder output is by calling the  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> method to create an array of 2D  textures. However, you cannot use texture arrays that are created with this flag in calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_BIND_VIDEO_ENCODER:0x400L

Set this flag to indicate that a  <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro">2D texture</a> is used to receive input from the video encoder API. The common way to create resources for a video encoder is by calling the  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> method to create an array of 2D  textures. However, you cannot use texture arrays that are created with this flag in calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

## -remarks

In general, binding flags can be combined using a bitwise OR (except the constant-buffer flag); however, you should use a single flag to allow the device to optimize the resource usage.

This enumeration is used by a:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">Buffer description</a> when creating a buffer.</li>
<li>Texture description when creating a texture (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture1d_desc">D3D11_TEXTURE1D_DESC</a> or <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a> or <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a>).</li>
</ul>
A shader-resource buffer is NOT a constant buffer; rather, it is a texture or buffer resource that is bound to a shader, that contains texture or buffer data (it is not limited to a single element type in the buffer). A shader-resource buffer is created with the D3D11_BIND_SHADER_RESOURCE flag and is bound to the pipeline using one of these APIs: <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshaderresources">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshaderresources">ID3D11DeviceContext::PSSetShaderResources</a>, or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">ID3D11DeviceContext::VSSetShaderResources</a>. Furthermore, a shader-resource buffer cannot use the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a> flag.

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
