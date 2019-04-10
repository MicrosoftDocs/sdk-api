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
product: Windows
targetos: Windows
req.typenames: D3D12_RESOURCE_STATES
req.redist: 
---

# D3D12_RESOURCE_STATES enumeration


## -description



          Specifies the state of a resource regarding how the resource is being used.
        


## -enum-fields




### -field D3D12_RESOURCE_STATE_COMMON

Applications should only transition to this state for accessing a resource across different graphics engine types.

Specifically, a resource must be in the COMMON state before being used on a COPY queue (when previous used on DIRECT/COMPUTE), and before being used on DIRECT/COMPUTE (when previously used on COPY). This restriction does not exist when accessing data between DIRECT and COMPUTE queues.

The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.
            For more information, in <a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>, find "common".
          

Additionally, textures must be in the COMMON state for CPU access to be legal, assuming the texture was created in a CPU-visible heap in the first place.


### -field D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER


            A subresource must be in this state when it is accessed by the 3D pipeline as a vertex buffer or constant buffer.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_INDEX_BUFFER


            A subresource must be in this state when it is accessed by the 3D pipeline as an index buffer.
            This is a read-only state.
          


### -field D3D12_RESOURCE_STATE_RENDER_TARGET


            The resource is used as a render target.
            A subresource must be in this state when it is rendered to or when it is cleared with <a href="https://msdn.microsoft.com/5AB13E36-A189-41B4-AEF8-B5C5831655DB">ID3D12GraphicsCommandList::ClearRenderTargetView</a>.
            This is a write-only state. To read from a render target as a shader resource the resource must be in either  D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE or D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE.


### -field D3D12_RESOURCE_STATE_UNORDERED_ACCESS


            The resource is used for unordered access.
            A subresource must be in this state when it is accessed by the 3D pipeline via an unordered access view.
            A subresource must also be in this state when it is cleared with <a href="https://msdn.microsoft.com/A048BF0C-9141-4DDF-91F9-B53464033A44">ID3D12GraphicsCommandList::ClearUnorderedAccessViewInt</a> or <a href="https://msdn.microsoft.com/6A19F429-D7B2-4A71-8904-31BFA1FD10C6">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</a>.
            This is a read/write state.
          


### -field D3D12_RESOURCE_STATE_DEPTH_WRITE

DEPTH_WRITE is a state which is mutually exclusive with other states. It should be used for <a href="https://msdn.microsoft.com/EF56EA6C-00DB-4231-B67D-B99811F51246">ID3D12GraphicsCommandList::ClearDepthStencilView</a> when the flags (see <a href="https://msdn.microsoft.com/F66672BC-1610-43F2-BF39-5F498183E3A5">D3D12_CLEAR_FLAGS</a>) indicate a given subresource should be cleared (otherwise the subresource state doesn't matter), or when using it in a writable depth stencil view (see <a href="https://msdn.microsoft.com/A968BFFF-8C26-4C8C-9AA4-7E9BB5B0DF1F">D3D12_DSV_FLAGS</a>) when the PSO has depth write enabled (see <a href="https://msdn.microsoft.com/C324F6EF-668A-4056-B538-A05329751554">D3D12_DEPTH_STENCIL_DESC</a>).



### -field D3D12_RESOURCE_STATE_DEPTH_READ

DEPTH_READ is a state which can be combined with other states. It should be used when the subresource is in a read-only depth stencil view, or when the <i>DepthEnable</i> parameter of <a href="https://msdn.microsoft.com/C324F6EF-668A-4056-B538-A05329751554">D3D12_DEPTH_STENCIL_DESC</a> is false. It can be combined with other read states (for example, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE), such that the resource can be used for the depth or stencil test, and accessed by a shader within the same draw call. Using it when depth will be written by a draw call or clear command is invalid.


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
            Subresources must be in this state when they are used as the argument buffer passed to the indirect drawing method <a href="https://msdn.microsoft.com/99FB088D-F3EB-4BAD-A945-51A1ED6F9288">ID3D12GraphicsCommandList::ExecuteIndirect</a>.
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


### -field D3D12_RESOURCE_STATE_GENERIC_READ

This is the required starting state for upload heaps. Applications should generally avoid this state when possible, and instead transition resources to only the actually-used states.


### -field D3D12_RESOURCE_STATE_PRESENT


            Synonymous with D3D12_RESOURCE_STATE_COMMON.
          


### -field D3D12_RESOURCE_STATE_PREDICATION


            The resource is used for <a href="https://msdn.microsoft.com/5C5138C7-F6E8-4646-961A-0E2312B5356B">Predication</a>.
          


### -field D3D12_RESOURCE_STATE_VIDEO_DECODE_READ


            The resource is used to read compressed video data during video decoding; that is, the resource is used as the source in a decode operation.
          


### -field D3D12_RESOURCE_STATE_VIDEO_DECODE_WRITE


            The resource is used to write decompressed video data during video decoding; that is, the resource is used as the destination in a decode operation.
          


### -field D3D12_RESOURCE_STATE_VIDEO_PROCESS_READ


            The resource is used to read video data during video processing; that is, the resource is used as the source in a processing operation such as video encoding (compression).
          


### -field D3D12_RESOURCE_STATE_VIDEO_PROCESS_WRITE


            The resource is used to write video data during video processing; that is, the resource is used as the destination in a processing operation such as video encoding (compression).
          


### -field D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ


### -field D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE




## -remarks




        This enum is used by the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">CreateCommittedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">CreateReservedResource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

