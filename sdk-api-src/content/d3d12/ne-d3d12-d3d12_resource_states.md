---
UID: NE:d3d12.D3D12_RESOURCE_STATES
title: D3D12_RESOURCE_STATES (d3d12.h)
author: windows-sdk-content
description: Specifies the state of a resource regarding how the resource is being used.
old-location: direct3d12\d3d12_resource_states.htm
tech.root: direct3d12
ms.assetid: AB14DE3E-97EA-47BE-8917-805B9651ED3A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_STATES, D3D12_RESOURCE_STATES enumeration, D3D12_RESOURCE_STATE_COMMON, D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_COPY_SOURCE, D3D12_RESOURCE_STATE_DEPTH_READ, D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_INDEX_BUFFER, D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT, D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_PREDICATION, D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_RESOLVE_DEST, D3D12_RESOURCE_STATE_RESOLVE_SOURCE, D3D12_RESOURCE_STATE_STREAM_OUT, D3D12_RESOURCE_STATE_UNORDERED_ACCESS, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER, D3D12_RESOURCE_STATE_VIDEO_DECODE_READ, D3D12_RESOURCE_STATE_VIDEO_DECODE_WRITE, D3D12_RESOURCE_STATE_VIDEO_PROCESS_READ, D3D12_RESOURCE_STATE_VIDEO_PROCESS_WRITE, d3d12/D3D12_RESOURCE_STATES, d3d12/D3D12_RESOURCE_STATE_COMMON, d3d12/D3D12_RESOURCE_STATE_COPY_DEST, d3d12/D3D12_RESOURCE_STATE_COPY_SOURCE, d3d12/D3D12_RESOURCE_STATE_DEPTH_READ, d3d12/D3D12_RESOURCE_STATE_DEPTH_WRITE, d3d12/D3D12_RESOURCE_STATE_GENERIC_READ, d3d12/D3D12_RESOURCE_STATE_INDEX_BUFFER, d3d12/D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT, d3d12/D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE, d3d12/D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, d3d12/D3D12_RESOURCE_STATE_PREDICATION, d3d12/D3D12_RESOURCE_STATE_PRESENT, d3d12/D3D12_RESOURCE_STATE_RENDER_TARGET, d3d12/D3D12_RESOURCE_STATE_RESOLVE_DEST, d3d12/D3D12_RESOURCE_STATE_RESOLVE_SOURCE, d3d12/D3D12_RESOURCE_STATE_STREAM_OUT, d3d12/D3D12_RESOURCE_STATE_UNORDERED_ACCESS, d3d12/D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER, d3d12/D3D12_RESOURCE_STATE_VIDEO_DECODE_READ, d3d12/D3D12_RESOURCE_STATE_VIDEO_DECODE_WRITE, d3d12/D3D12_RESOURCE_STATE_VIDEO_PROCESS_READ, d3d12/D3D12_RESOURCE_STATE_VIDEO_PROCESS_WRITE, direct3d12.d3d12_resource_states
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_RESOURCE_STATES"
dev_langs:
 - c++
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
 - D3D12_RESOURCE_STATES
targetos: Windows
req.typenames: D3D12_RESOURCE_STATES
req.redist: 
ms.custom: 19H1
---

# D3D12_RESOURCE_STATES enumeration


## -description



          Specifies the state of a resource regarding how the resource is being used.
        


## -enum-fields




### -field D3D12_RESOURCE_STATE_COMMON

Applications should only transition to this state for accessing a resource across different graphics engine types.

Specifically, a resource must be in the COMMON state before being used on a COPY queue (when previous used on DIRECT/COMPUTE), and before being used on DIRECT/COMPUTE (when previously used on COPY). This restriction does not exist when accessing data between DIRECT and COMPUTE queues.

The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.
            For more information, in <a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>, find "common".
          

Additionally, textures must be in the COMMON state for CPU access to be legal, assuming the texture was created in a CPU-visible heap in the first place.


### -field D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER


            A subresource must be in this state when it is accessed by the 3D pipeline as a vertex buffer or constant buffer.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_INDEX_BUFFER


            A subresource must be in this state when it is accessed by the 3D pipeline as an index buffer.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_RENDER_TARGET


            The resource is used as a render target.
            A subresource must be in this state when it is rendered to or when it is cleared with <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview">ID3D12GraphicsCommandList::ClearRenderTargetView</a>.
            This is a write-only state. To read from a render target as a shader resource the resource must be in either  D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE or D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE.


### -field D3D12_RESOURCE_STATE_UNORDERED_ACCESS


            The resource is used for unordered access.
            A subresource must be in this state when it is accessed by the 3D pipeline via an unordered access view.
            A subresource must also be in this state when it is cleared with <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint">ID3D12GraphicsCommandList::ClearUnorderedAccessViewInt</a> or <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>.
            This is a read/write state.
          


### -field D3D12_RESOURCE_STATE_DEPTH_WRITE

DEPTH_WRITE is a state which is mutually exclusive with other states. It should be used for <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview">ID3D12GraphicsCommandList::ClearDepthStencilView</a> when the flags (see <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags">D3D12_CLEAR_FLAGS</a>) indicate a given subresource should be cleared (otherwise the subresource state doesn't matter), or when using it in a writable depth stencil view (see <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags">D3D12_DSV_FLAGS</a>) when the PSO has depth write enabled (see <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a>).



### -field D3D12_RESOURCE_STATE_DEPTH_READ

DEPTH_READ is a state which can be combined with other states. It should be used when the subresource is in a read-only depth stencil view, or when the <i>DepthEnable</i> parameter of <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a> is false. It can be combined with other read states (for example, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE), such that the resource can be used for the depth or stencil test, and accessed by a shader within the same draw call. Using it when depth will be written by a draw call or clear command is invalid.


### -field D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE


            The resource is used with a shader other than the pixel shader.
            A subresource must be in this state before being read by any stage (except for the pixel shader stage) via a shader resource view.
            You can still use the resource in a pixel shader with this flag as long as it also has the flag D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE set. This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE


            The resource is used with a pixel shader.
            A subresource must be in this state before being read by the pixel shader via a shader resource view.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_STREAM_OUT


            The resource is used with stream output.
            A subresource must be in this state when it is accessed by the 3D pipeline as a stream-out target.
            This is a write-only state.
          


### -field D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT


            The resource is used as an indirect argument.
            Subresources must be in this state when they are used as the argument buffer passed to the indirect drawing method <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect">ID3D12GraphicsCommandList::ExecuteIndirect</a>.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_COPY_DEST


            The resource is used as the destination in a copy operation.
            Subresources must be in this state when they are used as the destination of copy operation, or a blt operation.
            This is a write-only state.
          


### -field D3D12_RESOURCE_STATE_COPY_SOURCE


            The resource is used as the source in a copy operation.
            Subresources must be in this state when they are used as the source of copy operation, or a blt operation.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_RESOLVE_DEST


            The resource is used as the destination in a resolve operation.
          


### -field D3D12_RESOURCE_STATE_RESOLVE_SOURCE


            The resource is used as the source in a resolve operation.
          


### -field D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE

### D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE

Starting with Windows 10, version 1903 (10.0; Build 18362), indicates that the resource is a screen-space shading-rate image for variable-rate shading (VRS). For more info, see [Variable-rate shading (VRS)](/windows/win32/direct3d12/vrs).

### -field D3D12_RESOURCE_STATE_GENERIC_READ

D3D12_RESOURCE_STATE_GENERIC_READ is a logically OR'd combination of other read-state bits. This is the required starting state for an upload heap. Your application should generally avoid transitioning to D3D12_RESOURCE_STATE_GENERIC_READ when possible, since that can result in premature cache flushes, or resource layout changes (for example, compress/decompress), causing unnecessary pipeline stalls. You should instead transition resources only to the actually-used states.

### -field D3D12_RESOURCE_STATE_PRESENT


            Synonymous with D3D12_RESOURCE_STATE_COMMON.
          


### -field D3D12_RESOURCE_STATE_PREDICATION


            The resource is used for <a href="/windows/win32/direct3d12/predication">Predication</a>.
          


### -field D3D12_RESOURCE_STATE_VIDEO_DECODE_READ


            The resource is used as a source in a decode operation. Examples include reading the compressed bitstream and reading from decode references,
          


### -field D3D12_RESOURCE_STATE_VIDEO_DECODE_WRITE


            The resource is used as a destination in the decode operation. This state is used for decode output and histograms.
          


### -field D3D12_RESOURCE_STATE_VIDEO_PROCESS_READ


            The resource is used to read video data during video processing; that is, the resource is used as the source in a processing operation such as video encoding (compression).
          


### -field D3D12_RESOURCE_STATE_VIDEO_PROCESS_WRITE


            The resource is used to write video data during video processing; that is, the resource is used as the destination in a processing operation such as video encoding (compression).
          


### -field D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ
        
            The resource is used as the source in an encode operation. This state is used for the input and reference of motion estimation.


### -field D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE

            This resource is used as the destination in an encode operation. This state is used for the destination texture of a resolve motion vector heap operation.


## -remarks




        This enum is used by the following methods:
        

<ul>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">CreateCommittedResource</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>
</li>
</ul>



## -see-also




<a href="/windows/win32/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/win32/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

