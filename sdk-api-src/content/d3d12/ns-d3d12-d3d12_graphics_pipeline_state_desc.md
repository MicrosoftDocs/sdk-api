---
UID: NS:d3d12.D3D12_GRAPHICS_PIPELINE_STATE_DESC
title: D3D12_GRAPHICS_PIPELINE_STATE_DESC (d3d12.h)
description: Describes a graphics pipeline state object.
helpviewer_keywords: ["D3D12_GRAPHICS_PIPELINE_STATE_DESC","D3D12_GRAPHICS_PIPELINE_STATE_DESC structure","d3d12/D3D12_GRAPHICS_PIPELINE_STATE_DESC","direct3d12.d3d12_graphics_pipeline_state_desc"]
old-location: direct3d12\d3d12_graphics_pipeline_state_desc.htm
tech.root: direct3d12
ms.assetid: 35D10150-A633-4D38-B684-3E2DF357FFC0
ms.date: 12/05/2018
ms.keywords: D3D12_GRAPHICS_PIPELINE_STATE_DESC, D3D12_GRAPHICS_PIPELINE_STATE_DESC structure, d3d12/D3D12_GRAPHICS_PIPELINE_STATE_DESC, direct3d12.d3d12_graphics_pipeline_state_desc
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
req.typenames: D3D12_GRAPHICS_PIPELINE_STATE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_GRAPHICS_PIPELINE_STATE_DESC
 - d3d12/D3D12_GRAPHICS_PIPELINE_STATE_DESC
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
 - D3D12_GRAPHICS_PIPELINE_STATE_DESC
---

# D3D12_GRAPHICS_PIPELINE_STATE_DESC structure


## -description

Describes a graphics pipeline state object.

## -struct-fields

### -field pRootSignature

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a> object.

### -field VS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the vertex shader.

### -field PS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the pixel shader.

### -field DS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the domain shader.

### -field HS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the hull shader.

### -field GS

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode">D3D12_SHADER_BYTECODE</a> structure that describes the geometry shader.

### -field StreamOutput

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc">D3D12_STREAM_OUTPUT_DESC</a> structure that describes a streaming output buffer.

### -field BlendState

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc">D3D12_BLEND_DESC</a> structure that describes the blend state.

### -field SampleMask

The sample mask for the blend state.

### -field RasterizerState

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc">D3D12_RASTERIZER_DESC</a> structure that describes the rasterizer state.

### -field DepthStencilState

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a> structure that describes the depth-stencil state.

### -field InputLayout

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc">D3D12_INPUT_LAYOUT_DESC</a> structure that describes the input-buffer data for the input-assembler stage.

### -field IBStripCutValue

Specifies the properties of the index buffer in a  <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value">D3D12_INDEX_BUFFER_STRIP_CUT_VALUE</a> structure.

### -field PrimitiveTopologyType

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type">D3D12_PRIMITIVE_TOPOLOGY_TYPE</a>-typed value for the type of primitive, and ordering of the primitive data.

### -field NumRenderTargets

The number of render target formats in the  <b>RTVFormats</b> member.

### -field RTVFormats

An array of <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed values for the render target formats.

### -field DSVFormat

A <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the depth-stencil format.

### -field SampleDesc

A <a href="/windows/win32/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a> structure that specifies multisampling parameters.

### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the graphics pipeline state is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -field CachedPSO

A cached pipeline state object, as a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state">D3D12_CACHED_PIPELINE_STATE</a> structure. pCachedBlob and CachedBlobSizeInBytes may be set to NULL and 0 respectively.

### -field Flags

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags">D3D12_PIPELINE_STATE_FLAGS</a> enumeration constant such as for "tool debug".

## -remarks

This structure is used by the <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate">CreateGraphicsPipelineState</a> method.
      

The runtime validates:
          

<ul>
<li>Whether the linkage between the shader stages is correct.
          </li>
<li>If the <b>HS</b> and <b>DS</b> members are specified, the <b>PrimitiveTopologyType</b> member for topology type must be set to <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type">D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH</a>.
          </li>
<li>Whether sample frequency execution isn't allowed with the center multi-sample anti-aliasing (MSAA) pattern.
          </li>
<li>Whether anti-aliasing lines aren't allowed with the center MSAA pattern.
          </li>
<li>
If the <b>ForcedSampleCount</b> member of <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc">D3D12_RASTERIZER_DESC</a> that <b>RasterizerState</b> specifies isn't zero:
              

<ul>
<li>Depth/stencil must be disabled.
              </li>
<li>Pixel shader can't output depth.
              </li>
<li>Pixel shader can't run at sample frequency.
              </li>
<li>Render target sample count must be 1.
              </li>
</ul>
</li>
<li>Whether blend state is compatible with render target formats.
          </li>
<li>Whether pixel shader output type is compatible with render target format.
          </li>
<li>Whether the sample count and quality are supported for the render target/depth stencil formats.
          </li>
</ul>

## -see-also

<a href="/windows/win32/direct3d12/conservative-rasterization">Conservative Rasterization</a>



<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/win32/direct3d12/rasterizer-order-views">Rasterizer Ordered Views</a>

