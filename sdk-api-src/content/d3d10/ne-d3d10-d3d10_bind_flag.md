---
UID: NE:d3d10.D3D10_BIND_FLAG
title: D3D10_BIND_FLAG (d3d10.h)
description: Identifies how to bind a resource to the pipeline.
helpviewer_keywords: ["7e986ece-3bd3-f96c-c7c8-27d21e16623f","D3D10_BIND_CONSTANT_BUFFER","D3D10_BIND_DEPTH_STENCIL","D3D10_BIND_FLAG","D3D10_BIND_FLAG enumeration [Direct3D 10]","D3D10_BIND_INDEX_BUFFER","D3D10_BIND_RENDER_TARGET","D3D10_BIND_SHADER_RESOURCE","D3D10_BIND_STREAM_OUTPUT","D3D10_BIND_VERTEX_BUFFER","d3d10/D3D10_BIND_CONSTANT_BUFFER","d3d10/D3D10_BIND_DEPTH_STENCIL","d3d10/D3D10_BIND_FLAG","d3d10/D3D10_BIND_INDEX_BUFFER","d3d10/D3D10_BIND_RENDER_TARGET","d3d10/D3D10_BIND_SHADER_RESOURCE","d3d10/D3D10_BIND_STREAM_OUTPUT","d3d10/D3D10_BIND_VERTEX_BUFFER","direct3d10.d3d10_bind_flag"]
old-location: direct3d10\d3d10_bind_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_bind_flag.htm
ms.date: 12/05/2018
ms.keywords: 7e986ece-3bd3-f96c-c7c8-27d21e16623f, D3D10_BIND_CONSTANT_BUFFER, D3D10_BIND_DEPTH_STENCIL, D3D10_BIND_FLAG, D3D10_BIND_FLAG enumeration [Direct3D 10], D3D10_BIND_INDEX_BUFFER, D3D10_BIND_RENDER_TARGET, D3D10_BIND_SHADER_RESOURCE, D3D10_BIND_STREAM_OUTPUT, D3D10_BIND_VERTEX_BUFFER, d3d10/D3D10_BIND_CONSTANT_BUFFER, d3d10/D3D10_BIND_DEPTH_STENCIL, d3d10/D3D10_BIND_FLAG, d3d10/D3D10_BIND_INDEX_BUFFER, d3d10/D3D10_BIND_RENDER_TARGET, d3d10/D3D10_BIND_SHADER_RESOURCE, d3d10/D3D10_BIND_STREAM_OUTPUT, d3d10/D3D10_BIND_VERTEX_BUFFER, direct3d10.d3d10_bind_flag
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_BIND_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BIND_FLAG
 - d3d10/D3D10_BIND_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BIND_FLAG
---

# D3D10_BIND_FLAG enumeration


## -description

Identifies how to bind a resource to the pipeline.

## -enum-fields

### -field D3D10_BIND_VERTEX_BUFFER:0x1L

Bind a buffer as a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">vertex buffer</a> to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

### -field D3D10_BIND_INDEX_BUFFER:0x2L

Bind a buffer as an <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">index buffer</a> to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

### -field D3D10_BIND_CONSTANT_BUFFER:0x4L

Bind a buffer as a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffer</a> to a <a href="/previous-versions/bb205146(v=vs.85)">shader stage</a>; this flag may NOT be combined with any other bind flag.

### -field D3D10_BIND_SHADER_RESOURCE:0x8L

Bind a buffer or texture to a <a href="/previous-versions/bb205146(v=vs.85)">shader stage</a>; this flag cannot be used with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP_WRITE_NO_OVERWRITE</a> flag.

### -field D3D10_BIND_STREAM_OUTPUT:0x10L

Bind an output buffer for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">stream-output stage</a>.

### -field D3D10_BIND_RENDER_TARGET:0x20L

Bind a texture as a render target for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

### -field D3D10_BIND_DEPTH_STENCIL:0x40L

Bind a texture as a depth-stencil target for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

## -remarks

In general, binding flags can be combined using a logical OR (except the constant-buffer flag); however, you should use a single flag to allow the device to optimize the resource usage.

This enumeration is used by a:

<ul>
<li>
<a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">Buffer description</a> when creating a buffer.</li>
<li>Texture description when creating a texture (see <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture1d_desc">D3D10_TEXTURE1D_DESC</a> or <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture2d_desc">D3D10_TEXTURE2D_DESC</a> or <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_texture3d_desc">D3D10_TEXTURE3D_DESC</a>).</li>
</ul>
A shader-resource buffer is NOT a constant buffer; rather, it is a texture or buffer resource that is bound to a shader, that contains texture or buffer data (it is not limited to a single element type in the buffer). A shader-resource buffer is created with the D3D10_BIND_SHADER_RESOURCE flag and is bound to the pipeline using one of these APIs: <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">ID3D10Device::GSSetShaderResources</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">ID3D10Device::PSSetShaderResources</a>, or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">ID3D10Device::VSSetShaderResources</a>. Furthermore, a shader-resource buffer cannot use the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP_WRITE_NO_OVERWRITE</a> flag.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
