---
UID: NF:d3d12.ID3D12GraphicsCommandList.BeginQuery
title: ID3D12GraphicsCommandList::BeginQuery
author: windows-sdk-content
description: Starts a query running.
old-location: direct3d12\id3d12graphicscommandlist_beginquery.htm
old-project: direct3d12
ms.assetid: 38011ED8-C867-4ECE-880F-3963A17790F7
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: BeginQuery, BeginQuery method, BeginQuery method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,BeginQuery method, ID3D12GraphicsCommandList.BeginQuery, ID3D12GraphicsCommandList::BeginQuery, d3d12/ID3D12GraphicsCommandList::BeginQuery, direct3d12.id3d12graphicscommandlist_beginquery
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
 - ID3D12GraphicsCommandList.BeginQuery
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::BeginQuery


## -description


Starts a query running.


## -parameters




### -param pQueryHeap [in]

Type: <b><a href="https://msdn.microsoft.com/330DE59A-8098-4255-85DD-0C439DD48250">ID3D12QueryHeap</a>*</b>

Specifies the <a href="https://msdn.microsoft.com/330DE59A-8098-4255-85DD-0C439DD48250">ID3D12QueryHeap</a> containing the query.
          


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/F6FA9ACE-0089-4C7B-99D7-FD286CF4B18D">D3D12_QUERY_TYPE</a></b>

Specifies one member of <a href="https://msdn.microsoft.com/F6FA9ACE-0089-4C7B-99D7-FD286CF4B18D">D3D12_QUERY_TYPE</a>.
          


### -param Index [in]

Type: <b>UINT</b>

Specifies the index of the query within the query heap.
          


## -returns



This method does not return a value.
          




## -remarks



In Direct3D 12, the usage of queries is more restricted than Direct3D 11.  The following scenarios are no longer supported:
        

<ul>
<li>A call to <b>BeginQuery</b> followed by another call to  <b>BeginQuery</b>  without an intervening call to <a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a>.
          </li>
<li>A call to <a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a> followed by <b>EndQuery</b>  without an intervening call to <b>BeginQuery</b>.
          </li>
</ul>
Given these restrictions, there are 3 states that a query can be in:
        

<ul>
<li>Inactive (this is the initial state of all queries)</li>
<li>Querying</li>
<li>Predicating</li>
</ul>
<b>BeginQuery</b> transitions a query from the inactive state to the querying state.
          <a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a> transitions a query from the querying state to the inactive state. <a href="https://msdn.microsoft.com/21526012-A675-40E8-A11C-4CBA5C12B9CF">SetPredication</a> transitions the previous set query from the predicating state to the inactive state and transitions the newly set query from the inactive state to the predicating state.
        

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
The runtime will issue errors for the following calls:
          

<ul>
<li>Calling <b>BeginQuery</b> on a query which is in the querying or predicating state.
            </li>
<li>Calling <a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a> on a query which is in the inactive or predicating state.
            </li>
<li>Calling <a href="https://msdn.microsoft.com/21526012-A675-40E8-A11C-4CBA5C12B9CF">SetPredication</a> on a query which is in the querying state.
            </li>
</ul>
Illegal API calls will result in <a href="https://msdn.microsoft.com/EA9F00AD-8506-4F3C-871E-A51ED69005BB">Close</a> returning an error or <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ExecuteCommandList</a> dropping the command list, and the device becoming removed.
            Note that predication state is not inherited by direct command lists.  All direct command lists begin with predication disabled.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors whenever the runtime validation fails.
            Refer also to <a href="https://msdn.microsoft.com/D7403B5D-7E1B-4DD2-AE45-52E1153233C6">Queries</a>.
          


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12PredicationQueries</a> sample uses 
			 <b>ID3D12GraphicsCommandList::BeginQuery</b> as follows:
        

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
See <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

