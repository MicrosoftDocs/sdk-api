---
UID: NS:d3d12.D3D12_GRAPHICS_PIPELINE_STATE_DESC
title: D3D12_GRAPHICS_PIPELINE_STATE_DESC (d3d12.h)
author: windows-sdk-content
description: Describes a graphics pipeline state object.
old-location: direct3d12\d3d12_graphics_pipeline_state_desc.htm
tech.root: direct3d12
ms.assetid: 35D10150-A633-4D38-B684-3E2DF357FFC0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_GRAPHICS_PIPELINE_STATE_DESC, D3D12_GRAPHICS_PIPELINE_STATE_DESC structure, d3d12/D3D12_GRAPHICS_PIPELINE_STATE_DESC, direct3d12.d3d12_graphics_pipeline_state_desc
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_GRAPHICS_PIPELINE_STATE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_GRAPHICS_PIPELINE_STATE_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_GRAPHICS_PIPELINE_STATE_DESC structure


## -description


Describes a graphics pipeline state object.
        


## -struct-fields




### -field pRootSignature

A pointer to the <a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a> object.
          


### -field VS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the vertex shader.
          


### -field PS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the pixel shader.
          


### -field DS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the domain shader.
          


### -field HS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the hull shader.
          


### -field GS

A <a href="https://msdn.microsoft.com/E2195755-A0C2-4824-A2EB-553F7909847F">D3D12_SHADER_BYTECODE</a> structure that describes the geometry shader.
          


### -field StreamOutput

A <a href="https://msdn.microsoft.com/9EFAA901-857B-40E3-B4B7-7C04D53BCA67">D3D12_STREAM_OUTPUT_DESC</a> structure that describes a streaming output buffer.
          


### -field BlendState

A <a href="https://msdn.microsoft.com/FFCA10AF-1081-4D4B-900D-C3692D0B5A91">D3D12_BLEND_DESC</a> structure that describes the blend state.
          


### -field SampleMask

The sample mask for the blend state.
          


### -field RasterizerState

A <a href="https://msdn.microsoft.com/52ECF841-72BE-44B7-BFB1-305B6981C1F4">D3D12_RASTERIZER_DESC</a> structure that describes the rasterizer state.
          


### -field DepthStencilState

A <a href="https://msdn.microsoft.com/C324F6EF-668A-4056-B538-A05329751554">D3D12_DEPTH_STENCIL_DESC</a> structure that describes the depth-stencil state.
          


### -field InputLayout

A <a href="https://msdn.microsoft.com/44C53830-AE80-402A-808C-2063011711A2">D3D12_INPUT_LAYOUT_DESC</a> structure that describes the input-buffer data for the input-assembler stage.
          


### -field IBStripCutValue

Specifies the properties of the index buffer in a  <a href="https://msdn.microsoft.com/22448EAE-05F3-4E14-90A6-A427E83361B8">D3D12_INDEX_BUFFER_STRIP_CUT_VALUE</a> structure.
          


### -field PrimitiveTopologyType

A <a href="https://msdn.microsoft.com/3BD4DF5E-EA91-4B2A-AADE-B9AE0E766F63">D3D12_PRIMITIVE_TOPOLOGY_TYPE</a>-typed value for the type of primitive, and ordering of the primitive data.
          


### -field NumRenderTargets

The number of render target formats in the  <b>RTVFormats</b> member.
          


### -field RTVFormats

An array of <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed values for the render target formats.
          


### -field DSVFormat

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value for the depth-stencil format.
          


### -field SampleDesc

A <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a> structure that specifies multisampling parameters.
          


### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the graphics pipeline state is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>.


### -field CachedPSO

A cached pipeline state object, as a <a href="https://msdn.microsoft.com/82A0CF70-7A16-45D5-A717-0BBB35DCC5A6">D3D12_CACHED_PIPELINE_STATE</a> structure.


### -field Flags

A <a href="https://msdn.microsoft.com/DAE5C06B-ED1F-4B35-812E-31E26B51704C">D3D12_PIPELINE_STATE_FLAGS</a> enumeration constant such as for "tool debug".
          


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">CreateGraphicsPipelineState</a> method.
      

The runtime validates:
          

<ul>
<li>Whether the linkage between the shader stages is correct.
          </li>
<li>If the <b>HS</b> and <b>DS</b> members are specified, the <b>PrimitiveTopologyType</b> member for topology type must be set to <a href="https://msdn.microsoft.com/en-us/library/Dn770385(v=VS.85).aspx">D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH</a>.
          </li>
<li>Whether sample frequency execution isn't allowed with the center multi-sample anti-aliasing (MSAA) pattern.
          </li>
<li>Whether anti-aliasing lines aren't allowed with the center MSAA pattern.
          </li>
<li>
If the <b>ForcedSampleCount</b> member of <a href="https://msdn.microsoft.com/52ECF841-72BE-44B7-BFB1-305B6981C1F4">D3D12_RASTERIZER_DESC</a> that <b>RasterizerState</b> specifies isn't zero:
              

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
<div class="alert"><b>Note</b>  You can create pipeline objects that don't specify any shader objects.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/081199AD-1702-4EC8-95AD-B1148C676199">Conservative Rasterization</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/D308BF3E-8CBE-4DF0-B020-4D202E858D99">Rasterizer Ordered Views</a>
 

 

