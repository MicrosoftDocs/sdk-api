---
UID: NF:d3d12.ID3D12GraphicsCommandList.ExecuteBundle
title: ID3D12GraphicsCommandList::ExecuteBundle
author: windows-sdk-content
description: Executes a bundle.
old-location: direct3d12\id3d12graphicscommandlist_executebundle.htm
tech.root: direct3d12
ms.assetid: B8AE4448-041D-47F6-9F0F-AE74FFEF6E41
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ExecuteBundle, ExecuteBundle method, ExecuteBundle method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ExecuteBundle method, ID3D12GraphicsCommandList.ExecuteBundle, ID3D12GraphicsCommandList::ExecuteBundle, d3d12/ID3D12GraphicsCommandList::ExecuteBundle, direct3d12.id3d12graphicscommandlist_executebundle
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
 - ID3D12GraphicsCommandList.ExecuteBundle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::ExecuteBundle


## -description


Executes a bundle.
        


## -parameters




### -param pCommandList [in]

Type: <b><a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>*</b>

Specifies the <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a> that determines the bundle to be executed.
          


## -returns



This method does not return a value.
          




## -remarks



Bundles inherit all state from the parent command list on which <b>ExecuteBundle</b> is called, except the pipeline state object and primitive topology.
        All of the state that is set in a bundle will affect the state of the parent command list.
        Note that <b>ExecuteBundle</b> is not a predicated operation.
      

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
The runtime will validate that the "callee" is a bundle and that the "caller" is a direct command list.  The runtime will also validate that the bundle has been closed.  If the contract is violated, the runtime will silently drop the call.
            Validation failure will result in <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> returning E_INVALIDARG.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue a warning in the same cases where the runtime will fail.
            The debug layer will issue a warning if a predicate is set when <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandList</a> is called.
            Also, the debug layer will issue an error if it detects that any resource reference by the command list has been destroyed.
          

The debug layer will also validate that the command allocator associated with the bundle has not been reset since <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> was called on the command list.  This validation occurs at <b>ExecuteBundle</b> time, and when the parent command list is executed on a command queue.
          


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12GraphicsCommandList::ExecuteBundle</b> as follows:
        

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
See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

