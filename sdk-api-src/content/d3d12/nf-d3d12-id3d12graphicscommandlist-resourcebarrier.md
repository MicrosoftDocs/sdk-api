---
UID: NF:d3d12.ID3D12GraphicsCommandList.ResourceBarrier
title: ID3D12GraphicsCommandList::ResourceBarrier
author: windows-sdk-content
description: Notifies the driver that it needs to synchronize multiple accesses to resources.
old-location: direct3d12\id3d12graphicscommandlist_resourcebarrier.htm
tech.root: direct3d12
ms.assetid: AA788F94-122B-4132-BED5-162EAC683676
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,ResourceBarrier method, ID3D12GraphicsCommandList.ResourceBarrier, ID3D12GraphicsCommandList::ResourceBarrier, ResourceBarrier, ResourceBarrier method, ResourceBarrier method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::ResourceBarrier, direct3d12.id3d12graphicscommandlist_resourcebarrier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.ResourceBarrier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::ResourceBarrier


## -description


Notifies the driver that it needs to synchronize multiple accesses to resources.
        


## -parameters




### -param NumBarriers [in]

Type: <b>UINT</b>

The number of submitted barrier descriptions.
          


### -param pBarriers [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn986740(v=VS.85).aspx">D3D12_RESOURCE_BARRIER</a>*</b>

Pointer to an array of barrier descriptions.
          


## -returns



This method does not return a value.
          




## -remarks



There are three types of barrier descriptions:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn986745(v=VS.85).aspx">D3D12_RESOURCE_TRANSITION_BARRIER</a> -  Transition barriers  indicate that a set of subresources transition between different usages.  The caller must specify the <i>before</i> and <i>after</i> usages of the subresources.  The D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES flag is used to transition all subresources in a resource at the same time.
          </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn986739(v=VS.85).aspx">D3D12_RESOURCE_ALIASING_BARRIER</a> - Aliasing barriers indicate a transition between usages of two different resources which have mappings into the same heap.  The application can specify both the before and the after resource.  Note that one or both resources can be NULL (indicating that any tiled resource could cause aliasing).
          </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn986746(v=VS.85).aspx">D3D12_RESOURCE_UAV_BARRIER</a> - Unordered access view barriers indicate all UAV accesses (read or writes) to a particular resource must complete before any future UAV accesses (read or write) can begin.  The specified resource may be NULL.  It is not necessary to insert a UAV barrier between two draw or dispatch calls which only read a UAV.  Additionally, it is not necessary to insert a UAV barrier between two draw or dispatch calls which write to the same UAV if the application knows that it is safe to execute the UAV accesses in any order.  The resource can be NULL (indicating that any UAV access could require the barrier).
          </li>
</ul>
When <b>ID3D12GraphicsCommandList::ResourceBarrier</b> is passed an array of resource barrier descriptions, the API behaves as if it was called N times (1 for each array element), in the specified order.
      Transitions should be batched together into a single API call when possible, as a performance optimization.

For descriptions of the usage states a subresource can be in, see the <a href="https://msdn.microsoft.com/en-us/library/Dn986744(v=VS.85).aspx">D3D12_RESOURCE_STATES</a> enumeration and the <a href="https://msdn.microsoft.com/en-us/library/Dn899226(v=VS.85).aspx">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a> section. 

All subresources in a resource must be in the RENDER_TARGET state, or DEPTH_WRITE state, for render targets/depth-stencil resources respectively, when  <a href="https://msdn.microsoft.com/en-us/library/Dn903869(v=VS.85).aspx">ID3D12GraphicsCommandList::DiscardResource</a> is called.
        

When a back buffer is presented, it must be in the D3D12_RESOURCE_STATE_PRESENT state.  If <a href="https://msdn.microsoft.com/en-us/library/Hh446797(v=VS.85).aspx">IDXGISwapChain1::Present1</a> is called on a resource which is not in the PRESENT state, a debug layer warning will be emitted.
      

The resource usage bits are group into two categories, read-only and read/write.

The following usage bits are read-only:
        

<ul>
<li>D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER</li>
<li>D3D12_RESOURCE_STATE_INDEX_BUFFER</li>
<li>D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</li>
<li>D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE</li>
<li>D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT</li>
<li>D3D12_RESOURCE_STATE_COPY_SOURCE</li>
<li>D3D12_RESOURCE_STATE_DEPTH_READ</li>
</ul>
The following usage bits are read/write:

<ul>
<li>D3D12_RESOURCE_STATE_UNORDERED_ACCESS</li>
<li>D3D12_RESOURCE_STATE_DEPTH_WRITE</li>
</ul>
The following usage bits are write-only:

<ul>
<li>D3D12_RESOURCE_STATE_COPY_DEST</li>
<li>D3D12_RESOURCE_STATE_RENDER_TARGET</li>
<li>D3D12_RESOURCE_STATE_STREAM_OUT</li>
</ul>
At most one write bit can be set.
          If any write bit is set, then no read bit may be set.
          If no write bit is set, then any number of read bits may be set.  

At any given time, a subresource is in exactly one  state (determined by a set of flags).  The application must ensure that the states are matched when making a sequence of <b>ResourceBarrier</b> calls. In other words, the before and after states in consecutive calls to <b>ResourceBarrier</b> must agree.
        

To transition all subresources within a resource, the application can set the subresource index to D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, which implies that all subresources are changed.

For improved performance, applications should use split barriers (refer to
        <a href="https://msdn.microsoft.com/en-us/library/Dn899217(v=VS.85).aspx">Synchronization and Multi-Engine</a>). Applications should also batch multiple transitions into a single call whenever possible.
      

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
The runtime will validate that the barrier type values are valid members of the <a href="https://msdn.microsoft.com/en-us/library/Dn770393(v=VS.85).aspx">D3D12_RESOURCE_BARRIER_TYPE</a> enumeration.
          

In addition, the runtime checks the following:
          

<ul>
<li>The resource pointer is non-NULL.</li>
<li>The subresource index is valid</li>
<li>The before and after states are supported by the <a href="https://msdn.microsoft.com/en-us/library/Dn770394(v=VS.85).aspx">D3D12_RESOURCE_BINDING_TIER</a> and <a href="https://msdn.microsoft.com/en-us/library/Dn986742(v=VS.85).aspx">D3D12_RESOURCE_FLAGS</a> flags of the resource.
            </li>
<li>Reserved bits in the state masks are not set.</li>
<li>The before and after states are different.</li>
<li>The set of bits in the before and after states are valid.</li>
<li>If the D3D12_RESOURCE_STATE_RESOLVE_SOURCE bit is set, then the resource sample count must be greater than 1.</li>
<li>If the D3D12_RESOURCE_STATE_RESOLVE_DEST bit is set, then the resource sample count must be equal to 1.</li>
</ul>
For aliasing barriers the runtime will validate that, if either resource pointer is non-NULL, it refers to a tiled resource.

For UAV barriers the runtime will validate that, if the resource is non-NULL, the resource has the D3D12_RESOURCE_STATE_UNORDERED_ACCESS bind flag set.
          

Validation failure causes <a href="https://msdn.microsoft.com/en-us/library/Dn903855(v=VS.85).aspx">ID3D12GraphicsCommandList::Close</a> to return E_INVALIDARG.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer normally issues errors where runtime validation fails:

<ul>
<li>If a  subresource transition in a command list is inconsistent with previous transitions in the same command list. </li>
<li>If a resource is used without first calling <b>ResourceBarrier</b> to put the resource into the correct state.  </li>
<li>If a resource is illegally bound for read and write at the same time.</li>
<li>If the <i>before</i> states passed to the <b>ResourceBarrier</b> do not match the <i>after</i> states of previous calls to <b>ResourceBarrier</b>, including the aliasing case.
            </li>
</ul>
Whereas the debug layer attempts to validate the runtime rules, it operates conservatively so that debug layer errors are real errors, and in some cases real errors may not produce debug layer errors. 

The debug layer will issue warnings in the following cases:

<ul>
<li>All of the cases where the D3D11 debug layer would issues warnings for <a href="https://msdn.microsoft.com/en-us/library/Dn280507(v=VS.85).aspx">ID3D11DeviceContext2::TiledResourceBarrier</a>.
            </li>
<li>If a depth buffer is used in a non-read-only mode while the resource has the D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE usage bit set.</li>
</ul>

#### Examples

The <a href="https://msdn.microsoft.com/en-us/library/Mt186624(v=VS.85).aspx">D3D12HelloTriangle</a> sample uses <b>ID3D12GraphicsCommandList::ResourceBarrier</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr&lt;IDXGISwapChain3&gt; m_swapChain;
ComPtr&lt;ID3D12Device&gt; m_device;
ComPtr&lt;ID3D12Resource&gt; m_renderTargets[FrameCount];
ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocator;
ComPtr&lt;ID3D12CommandQueue&gt; m_commandQueue;
ComPtr&lt;ID3D12RootSignature&gt; m_rootSignature;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_rtvHeap;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
UINT m_rtvDescriptorSize;
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator-&gt;Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList-&gt;Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList-&gt;SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList-&gt;RSSetViewports(1, &amp;m_viewport);
    m_commandList-&gt;RSSetScissorRects(1, &amp;m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList-&gt;OMSetRenderTargets(1, &amp;rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList-&gt;ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList-&gt;IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList-&gt;IASetVertexBuffers(0, 1, &amp;m_vertexBufferView);
    m_commandList-&gt;DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>
See <a href="https://msdn.microsoft.com/en-us/library/Dn933255(v=VS.85).aspx">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://www.youtube.com/watch?v=nmB2XMasz2o">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn903537(v=VS.85).aspx">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899226(v=VS.85).aspx">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

