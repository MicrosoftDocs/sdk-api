---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetPredication
title: ID3D12GraphicsCommandList::SetPredication (d3d12.h)
description: Sets a rendering predicate.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetPredication method","ID3D12GraphicsCommandList.SetPredication","ID3D12GraphicsCommandList::SetPredication","SetPredication","SetPredication method","SetPredication method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetPredication","direct3d12.id3d12graphicscommandlist_setpredication"]
old-location: direct3d12\id3d12graphicscommandlist_setpredication.htm
tech.root: direct3d12
ms.assetid: 21526012-A675-40E8-A11C-4CBA5C12B9CF
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetPredication method, ID3D12GraphicsCommandList.SetPredication, ID3D12GraphicsCommandList::SetPredication, SetPredication, SetPredication method, SetPredication method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetPredication, direct3d12.id3d12graphicscommandlist_setpredication
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
 - ID3D12GraphicsCommandList::SetPredication
 - d3d12/ID3D12GraphicsCommandList::SetPredication
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
 - ID3D12GraphicsCommandList.SetPredication
---

# ID3D12GraphicsCommandList::SetPredication


## -description

Sets a rendering predicate.

## -parameters

### -param pBuffer [in, optional]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

The buffer, as an <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>, which must be in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) or [**D3D21_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state (both values are identical, and provided as aliases for clarity), or **NULL** to disable predication.

### -param AlignedBufferOffset [in]

Type: <b>UINT64</b>

The aligned buffer offset, as a UINT64.

### -param Operation [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op">D3D12_PREDICATION_OP</a></b>

Specifies a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op">D3D12_PREDICATION_OP</a>, such as D3D12_PREDICATION_OP_EQUAL_ZERO or D3D12_PREDICATION_OP_NOT_EQUAL_ZERO.

## -remarks

Use this method to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting predicate data of the predicate is equal to the operation specified.
        

Unlike Direct3D 11, in Direct3D 12 predication state is not inherited by direct command lists, and predication is always respected (there are no predication hints).
        All direct command lists begin with predication disabled.
          Bundles do inherit predication state.
        It is legal for the same predicate to be bound multiple times.
      

Illegal API calls will result in <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> returning an error,
            or <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ID3D12CommandQueue::ExecuteCommandLists</a> dropping the command list and removing the device.
          

The debug layer will issue errors whenever the runtime validation fails.
          

Refer to <a href="/windows/desktop/direct3d12/predication">Predication</a> for more information.
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12PredicationQueries</a> sample uses <b>ID3D12GraphicsCommandList::SetPredication</b> as follows:
        


```cpp
// Fill the command list with all the render commands and dependent state.
void D3D12PredicationQueries::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_cbvHeap.Get() };
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
    m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Draw the quads and perform the occlusion query.
    {
        CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
        CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

        m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
        m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

        // Draw the far quad conditionally based on the result of the occlusion query
        // from the previous frame.
        m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
        m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
        m_commandList->DrawInstanced(4, 1, 0, 0);

        // Disable predication and always draw the near quad.
        m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
        m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
        m_commandList->DrawInstanced(4, 1, 4, 0);

        // Run the occlusion query with the bounding box quad.
        m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
        m_commandList->SetPipelineState(m_queryState.Get());
        m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
        m_commandList->DrawInstanced(4, 1, 8, 0);
        m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

        // Resolve the occlusion query and store the results in the query result buffer
        // to be used on the subsequent frame.
        m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_PREDICATION, D3D12_RESOURCE_STATE_COPY_DEST));
        m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
        m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PREDICATION));
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



<a href="/windows/desktop/direct3d12/predication-queries">Predication queries walk-through</a>
