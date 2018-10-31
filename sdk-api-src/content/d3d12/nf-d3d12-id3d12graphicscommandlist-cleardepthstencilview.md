---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearDepthStencilView
title: ID3D12GraphicsCommandList::ClearDepthStencilView
author: windows-sdk-content
description: Clears the depth-stencil resource.
old-location: direct3d12\id3d12graphicscommandlist_cleardepthstencilview.htm
tech.root: direct3d12
ms.assetid: EF56EA6C-00DB-4231-B67D-B99811F51246
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ClearDepthStencilView, ClearDepthStencilView method, ClearDepthStencilView method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearDepthStencilView method, ID3D12GraphicsCommandList.ClearDepthStencilView, ID3D12GraphicsCommandList::ClearDepthStencilView, d3d12/ID3D12GraphicsCommandList::ClearDepthStencilView, direct3d12.id3d12graphicscommandlist_cleardepthstencilview
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
 - ID3D12GraphicsCommandList.ClearDepthStencilView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::ClearDepthStencilView


## -description


Clears the depth-stencil resource.


## -parameters




### -param DepthStencilView [in]

Type: <b><a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap for the depth stencil to be cleared.
          


### -param ClearFlags [in]

Type: <b><a href="https://msdn.microsoft.com/F66672BC-1610-43F2-BF39-5F498183E3A5">D3D12_CLEAR_FLAGS</a></b>

A combination of <a href="https://msdn.microsoft.com/F66672BC-1610-43F2-BF39-5F498183E3A5">D3D12_CLEAR_FLAGS</a> values that are combined by using a bitwise OR operation. The resulting value identifies the type of data to clear (depth buffer, stencil buffer, or both).
          


### -param Depth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

A value to clear the depth buffer with. This value will be clamped between 0 and 1.
          


### -param Stencil [in]

Type: <b>UINT8</b>

A value to clear the stencil buffer with.
          


### -param NumRects [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rectangles in the array that the <i>pRects</i> parameter specifies.
          


### -param pRects [in]

Type: <b>const <b>D3D12_RECT</b>*</b>

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource view to clear. If <b>NULL</b>, <b>ClearDepthStencilView</b> clears the entire resource view.
          


## -returns



Returns nothing.
          




## -remarks



<b>ClearDepthStencilView</b> may be used to initialize resources which alias the same heap memory. See <a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a> for more details.

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
For floating-point inputs, the runtime will set denormalized values to 0 (while preserving NANs).
          

Validation failure will result in the call to <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> returning <b>E_INVALIDARG</b>.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors if the input colors are denormalized.
          

The debug layer will issue an error if the subresources referenced by the view are not in the appropriate state.
            For <b>ClearDepthStencilView</b>, the state must be in the state <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_DEPTH_WRITE</a>.
          


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12GraphicsCommandList::ClearDepthStencilView</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Pipeline objects.
D3D12_VIEWPORT m_viewport;
ComPtr&lt;IDXGISwapChain3&gt; m_swapChain;
ComPtr&lt;ID3D12Device&gt; m_device;
ComPtr&lt;ID3D12Resource&gt; m_renderTargets[FrameCount];
ComPtr&lt;ID3D12Resource&gt; m_depthStencil;
ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocator;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
ComPtr&lt;ID3D12CommandQueue&gt; m_commandQueue;
ComPtr&lt;ID3D12RootSignature &gt;m_rootSignature;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_rtvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_cbvSrvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_dsvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_samplerHeap;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState1;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState2;
D3D12_RECT m_scissorRect;
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
<pre>void D3D12Bundles::PopulateCommandList(FrameResource* pFrameResource)
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_pCurrentFrameResource-&gt;m_commandAllocator-&gt;Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList-&gt;Reset(m_pCurrentFrameResource-&gt;m_commandAllocator.Get(), m_pipelineState1.Get()));

    // Set necessary state.
    m_commandList-&gt;SetGraphicsRootSignature(m_rootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvHeap.Get(), m_samplerHeap.Get() };
    m_commandList-&gt;SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList-&gt;RSSetViewports(1, &amp;m_viewport);
    m_commandList-&gt;RSSetScissorRects(1, &amp;m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap-&gt;GetCPUDescriptorHandleForHeapStart());
    m_commandList-&gt;OMSetRenderTargets(1, &amp;rtvHandle, FALSE, &amp;dsvHandle);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList-&gt;ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList-&gt;ClearDepthStencilView(m_dsvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    if (UseBundles)
    {
        // Execute the prebuilt bundle.
        m_commandList-&gt;ExecuteBundle(pFrameResource-&gt;m_bundle.Get());
    }
    else
    {
        // Populate a new command list.
        pFrameResource-&gt;PopulateCommandList(m_commandList.Get(), m_pipelineState1.Get(), m_pipelineState2.Get(), m_currentFrameResourceIndex, m_numIndices, &amp;m_indexBufferView,
            &amp;m_vertexBufferView, m_cbvSrvHeap.Get(), m_cbvSrvDescriptorSize, m_samplerHeap.Get(), m_rootSignature.Get());
    }

    // Indicate that the back buffer will now be used to present.
    m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>
The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Multithreading</a> sample uses <b>ID3D12GraphicsCommandList::ClearDepthStencilView</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i &lt; CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]-&gt;Reset());
        ThrowIfFailed(m_commandLists[i]-&gt;Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]-&gt;ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i &lt; NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]-&gt;Reset());
        ThrowIfFailed(m_shadowCommandLists[i]-&gt;Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]-&gt;Reset());
        ThrowIfFailed(m_sceneCommandLists[i]-&gt;Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
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
<pre>// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource-&gt;Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource-&gt;m_commandLists[CommandListPre]-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource-&gt;m_commandLists[CommandListPre]-&gt;ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource-&gt;m_commandLists[CommandListPre]-&gt;ClearDepthStencilView(m_dsvHeap-&gt;GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource-&gt;m_commandLists[CommandListPre]-&gt;Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource-&gt;SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource-&gt;m_commandLists[CommandListMid]-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>
See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

