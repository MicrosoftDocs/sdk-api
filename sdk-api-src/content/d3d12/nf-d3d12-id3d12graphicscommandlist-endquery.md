---
UID: NF:d3d12.ID3D12GraphicsCommandList.EndQuery
title: ID3D12GraphicsCommandList::EndQuery
author: windows-sdk-content
description: Ends a running query.
old-location: direct3d12\id3d12graphicscommandlist_endquery.htm
old-project: direct3d12
ms.assetid: 591B277C-44C7-4C21-86B1-239F6A71308D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: EndQuery, EndQuery method, EndQuery method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,EndQuery method, ID3D12GraphicsCommandList.EndQuery, ID3D12GraphicsCommandList::EndQuery, d3d12/ID3D12GraphicsCommandList::EndQuery, direct3d12.id3d12graphicscommandlist_endquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.EndQuery
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::EndQuery


## -description


Ends a running query.
        


## -parameters




### -param pQueryHeap [in]

Type: <b><a href="https://msdn.microsoft.com/330DE59A-8098-4255-85DD-0C439DD48250">ID3D12QueryHeap</a>*</b>

Specifies the <a href="https://msdn.microsoft.com/330DE59A-8098-4255-85DD-0C439DD48250">ID3D12QueryHeap</a> containing the query.
          


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn903812(v=VS.85).aspx">D3D12_QUERY_TYPE</a></b>

Specifies one member of <a href="https://msdn.microsoft.com/en-us/library/Dn903812(v=VS.85).aspx">D3D12_QUERY_TYPE</a>.
          


### -param Index [in]

Type: <b>UINT</b>

Specifies the index of the query in the query heap.
          


## -returns



This method does not return a value.
          




## -remarks



Refer to the remarks for <a href="https://msdn.microsoft.com/en-us/library/Dn903838(v=VS.85).aspx">BeginQuery</a>, and to <a href="https://msdn.microsoft.com/D7403B5D-7E1B-4DD2-AE45-52E1153233C6">Queries</a>.
        


#### Examples

The <a href="https://msdn.microsoft.com/en-us/library/Mt186624(v=VS.85).aspx">D3D12PredicationQueries</a> sample uses <b>ID3D12GraphicsCommandList::EndQuery</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Fill the command list with all the render commands and dependent state.
void D3D12PredicationQueries::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]-&gt;Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList-&gt;Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList-&gt;SetGraphicsRootSignature(m_rootSignature.Get());

    ID3D12DescriptorHeap* ppHeaps[] = { m_cbvHeap.Get() };
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
    m_commandList-&gt;ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Draw the quads and perform the occlusion query.
    {
        CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap-&gt;GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
        CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

        m_commandList-&gt;IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
        m_commandList-&gt;IASetVertexBuffers(0, 1, &amp;m_vertexBufferView);

        // Draw the far quad conditionally based on the result of the occlusion query
        // from the previous frame.
        m_commandList-&gt;SetGraphicsRootDescriptorTable(0, cbvFarQuad);
        m_commandList-&gt;SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
        m_commandList-&gt;DrawInstanced(4, 1, 0, 0);

        // Disable predication and always draw the near quad.
        m_commandList-&gt;SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
        m_commandList-&gt;SetGraphicsRootDescriptorTable(0, cbvNearQuad);
        m_commandList-&gt;DrawInstanced(4, 1, 4, 0);

        // Run the occlusion query with the bounding box quad.
        m_commandList-&gt;SetGraphicsRootDescriptorTable(0, cbvFarQuad);
        m_commandList-&gt;SetPipelineState(m_queryState.Get());
        m_commandList-&gt;BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
        m_commandList-&gt;DrawInstanced(4, 1, 8, 0);
        m_commandList-&gt;EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

        // Resolve the occlusion query and store the results in the query result buffer
        // to be used on the subsequent frame.
        m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_PREDICATION, D3D12_RESOURCE_STATE_COPY_DEST));
        m_commandList-&gt;ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
        m_commandList-&gt;ResourceBarrier(1, &amp;CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PREDICATION));
    }

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




<a href="https://msdn.microsoft.com/en-us/library/Dn903537(v=VS.85).aspx">ID3D12GraphicsCommandList</a>
 

 

