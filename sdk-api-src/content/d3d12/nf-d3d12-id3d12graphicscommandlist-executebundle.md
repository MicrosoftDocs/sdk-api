---
UID: NF:d3d12.ID3D12GraphicsCommandList.ExecuteBundle
title: ID3D12GraphicsCommandList::ExecuteBundle (d3d12.h)
description: Executes a bundle.
helpviewer_keywords: ["ExecuteBundle","ExecuteBundle method","ExecuteBundle method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","ExecuteBundle method","ID3D12GraphicsCommandList.ExecuteBundle","ID3D12GraphicsCommandList::ExecuteBundle","d3d12/ID3D12GraphicsCommandList::ExecuteBundle","direct3d12.id3d12graphicscommandlist_executebundle"]
old-location: direct3d12\id3d12graphicscommandlist_executebundle.htm
tech.root: direct3d12
ms.assetid: B8AE4448-041D-47F6-9F0F-AE74FFEF6E41
ms.date: 12/05/2018
ms.keywords: ExecuteBundle, ExecuteBundle method, ExecuteBundle method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ExecuteBundle method, ID3D12GraphicsCommandList.ExecuteBundle, ID3D12GraphicsCommandList::ExecuteBundle, d3d12/ID3D12GraphicsCommandList::ExecuteBundle, direct3d12.id3d12graphicscommandlist_executebundle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::ExecuteBundle
 - d3d12/ID3D12GraphicsCommandList::ExecuteBundle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.ExecuteBundle
---

# ID3D12GraphicsCommandList::ExecuteBundle


## -description

Executes a bundle.

## -parameters

### -param pCommandList [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>*</b>

Specifies the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a> that determines the bundle to be executed.

## -remarks

Bundles inherit all state from the parent command list on which <b>ExecuteBundle</b> is called, except the pipeline state object and primitive topology.
        All of the state that is set in a bundle will affect the state of the parent command list.
        Note that <b>ExecuteBundle</b> is not a predicated operation.
      

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
The runtime will validate that the "callee" is a bundle and that the "caller" is a direct command list.  The runtime will also validate that the bundle has been closed.  If the contract is violated, the runtime will silently drop the call.
            Validation failure will result in <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> returning E_INVALIDARG.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue a warning in the same cases where the runtime will fail.
            The debug layer will issue a warning if a predicate is set when <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ExecuteCommandList</a> is called.
            Also, the debug layer will issue an error if it detects that any resource reference by the command list has been destroyed.
          

The debug layer will also validate that the command allocator associated with the bundle has not been reset since <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> was called on the command list.  This validation occurs at <b>ExecuteBundle</b> time, and when the parent command list is executed on a command queue.
          


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12GraphicsCommandList::ExecuteBundle</b> as follows:
        


```cpp
void D3D12Bundles::PopulateCommandList(FrameResource* pFrameResource)
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_pCurrentFrameResource->m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_pCurrentFrameResource->m_commandAllocator.Get(), m_pipelineState1.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvHeap.Get(), m_samplerHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    if (UseBundles)
    {
        // Execute the prebuilt bundle.
        m_commandList->ExecuteBundle(pFrameResource->m_bundle.Get());
    }
    else
    {
        // Populate a new command list.
        pFrameResource->PopulateCommandList(m_commandList.Get(), m_pipelineState1.Get(), m_pipelineState2.Get(), m_currentFrameResourceIndex, m_numIndices, &m_indexBufferView,
            &m_vertexBufferView, m_cbvSrvHeap.Get(), m_cbvSrvDescriptorSize, m_samplerHeap.Get(), m_rootSignature.Get());
    }

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}

```


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>