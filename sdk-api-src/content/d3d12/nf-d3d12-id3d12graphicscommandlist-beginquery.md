---
UID: NF:d3d12.ID3D12GraphicsCommandList.BeginQuery
title: ID3D12GraphicsCommandList::BeginQuery (d3d12.h)
author: windows-sdk-content
description: Starts a query running.
old-location: direct3d12\id3d12graphicscommandlist_beginquery.htm
tech.root: direct3d12
ms.assetid: 38011ED8-C867-4ECE-880F-3963A17790F7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginQuery, BeginQuery method, BeginQuery method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,BeginQuery method, ID3D12GraphicsCommandList.BeginQuery, ID3D12GraphicsCommandList::BeginQuery, d3d12/ID3D12GraphicsCommandList::BeginQuery, direct3d12.id3d12graphicscommandlist_beginquery
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
 - ID3D12GraphicsCommandList.BeginQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12GraphicsCommandList::BeginQuery


## -description


Starts a query running.


## -parameters




### -param pQueryHeap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap">ID3D12QueryHeap</a>*</b>

Specifies the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12queryheap">ID3D12QueryHeap</a> containing the query.
          


### -param Type [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type">D3D12_QUERY_TYPE</a></b>

Specifies one member of <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type">D3D12_QUERY_TYPE</a>.
          


### -param Index [in]

Type: <b>UINT</b>

Specifies the index of the query within the query heap.
          


## -returns



This method does not return a value.
          




## -remarks



In Direct3D 12, the usage of queries is more restricted than Direct3D 11.  The following scenarios are no longer supported:
        

<ul>
<li>A call to <b>BeginQuery</b> followed by another call to  <b>BeginQuery</b>  without an intervening call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery">EndQuery</a>.
          </li>
<li>A call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery">EndQuery</a> followed by <b>EndQuery</b>  without an intervening call to <b>BeginQuery</b>.
          </li>
</ul>
Given these restrictions, there are 3 states that a query can be in:
        

<ul>
<li>Inactive (this is the initial state of all queries)</li>
<li>Querying</li>
<li>Predicating</li>
</ul>
<b>BeginQuery</b> transitions a query from the inactive state to the querying state.
          <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery">EndQuery</a> transitions a query from the querying state to the inactive state. <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication">SetPredication</a> transitions the previous set query from the predicating state to the inactive state and transitions the newly set query from the inactive state to the predicating state.
        

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
The runtime will issue errors for the following calls:
          

<ul>
<li>Calling <b>BeginQuery</b> on a query which is in the querying or predicating state.
            </li>
<li>Calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery">EndQuery</a> on a query which is in the inactive or predicating state.
            </li>
<li>Calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication">SetPredication</a> on a query which is in the querying state.
            </li>
</ul>
Illegal API calls will result in <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> returning an error or <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ExecuteCommandList</a> dropping the command list, and the device becoming removed.
            Note that predication state is not inherited by direct command lists.  All direct command lists begin with predication disabled.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors whenever the runtime validation fails.
            Refer also to <a href="https://docs.microsoft.com/windows/desktop/direct3d12/queries">Queries</a>.
          


#### Examples

The <a href="https://docs.microsoft.com/windows/desktop/direct3d12/working-samples">D3D12PredicationQueries</a> sample uses 
			 <b>ID3D12GraphicsCommandList::BeginQuery</b> as follows:
        


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


See <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
 

 

