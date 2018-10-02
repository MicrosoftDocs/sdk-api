---
UID: NN:d3d12.ID3D12PipelineState
title: ID3D12PipelineState
author: windows-sdk-content
description: Represents the state of all currently set shaders as well as certain fixed function state objects.
old-location: direct3d12\id3d12pipelinestate.htm
tech.root: direct3d12
ms.assetid: DD922194-8AD2-4ADF-9AC2-46C903C56AE6
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ID3D12PipelineState, ID3D12PipelineState interface, ID3D12PipelineState interface,described, d3d12/ID3D12PipelineState, direct3d12.id3d12pipelinestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12PipelineState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12PipelineState interface


## -description


Represents the state of all currently set shaders as well as certain fixed function state objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12PipelineState</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12PipelineState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12PipelineState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/318FCFEE-74A7-4546-989E-9AF674D2B853">GetCachedBlob</a>
</td>
<td align="left" width="63%">
Gets the cached blob representing the pipeline state.
        

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">ID3D12Device::CreateGraphicsPipelineState</a> or  <a href="https://msdn.microsoft.com/FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57">ID3D12Device::CreateComputePipelineState</a> to create a pipeline state object (PSO). 

A pipeline state object corresponds to a significant portion of the state of the graphics processing unit (GPU).  This state includes all currently set shaders and certain fixed function state objects.  The only way to change states contained within the pipeline object is to change the currently bound pipeline object.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12DynamicIndexing</a> sample uses <b>ID3D12PipelineState</b> as follows:
        

Declare the pipeline objects.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Asset objects.
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState;
ComPtr&lt;ID3D12PipelineState&gt; m_computeState;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
ComPtr&lt;ID3D12Resource&gt; m_vertexBuffer;
ComPtr&lt;ID3D12Resource&gt; m_vertexBufferUpload;
D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;
ComPtr&lt;ID3D12Resource&gt; m_particleBuffer0[ThreadCount];
ComPtr&lt;ID3D12Resource&gt; m_particleBuffer1[ThreadCount];
ComPtr&lt;ID3D12Resource&gt; m_particleBuffer0Upload[ThreadCount];
ComPtr&lt;ID3D12Resource&gt; m_particleBuffer1Upload[ThreadCount];
ComPtr&lt;ID3D12Resource&gt; m_constantBufferGS;
UINT8* m_pConstantBufferGSData;
ComPtr&lt;ID3D12Resource&gt; m_constantBufferCS;
</pre>
</td>
</tr>
</table></span></div>
Initializing a bundle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void FrameResource::InitBundle(ID3D12Device* pDevice, ID3D12PipelineState* pPso,
    UINT frameResourceIndex, UINT numIndices, D3D12_INDEX_BUFFER_VIEW* pIndexBufferViewDesc, D3D12_VERTEX_BUFFER_VIEW* pVertexBufferViewDesc,
    ID3D12DescriptorHeap* pCbvSrvDescriptorHeap, UINT cbvSrvDescriptorSize, ID3D12DescriptorHeap* pSamplerDescriptorHeap, ID3D12RootSignature* pRootSignature)
{
    ThrowIfFailed(pDevice-&gt;CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_BUNDLE, m_bundleAllocator.Get(), pPso, IID_PPV_ARGS(&amp;m_bundle)));

    PopulateCommandList(m_bundle.Get(), pPso, frameResourceIndex, numIndices, pIndexBufferViewDesc,
        pVertexBufferViewDesc, pCbvSrvDescriptorHeap, cbvSrvDescriptorSize, pSamplerDescriptorHeap, pRootSignature);

    ThrowIfFailed(m_bundle-&gt;Close());
}
</pre>
</td>
</tr>
</table></span></div>
The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12PipelineState</b> as follows:
        

Populating the command lists, note the alternating PSO.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void FrameResource::PopulateCommandList(ID3D12GraphicsCommandList* pCommandList, ID3D12PipelineState* pPso1, ID3D12PipelineState* pPso2,
    UINT frameResourceIndex, UINT numIndices, D3D12_INDEX_BUFFER_VIEW* pIndexBufferViewDesc, D3D12_VERTEX_BUFFER_VIEW* pVertexBufferViewDesc,
    ID3D12DescriptorHeap* pCbvSrvDescriptorHeap, UINT cbvSrvDescriptorSize, ID3D12DescriptorHeap* pSamplerDescriptorHeap, ID3D12RootSignature* pRootSignature)
{
    // If the root signature matches the root signature of the caller, then
    // bindings are inherited, otherwise the bind space is reset.
    pCommandList-&gt;SetGraphicsRootSignature(pRootSignature);

    ID3D12DescriptorHeap* ppHeaps[] = { pCbvSrvDescriptorHeap, pSamplerDescriptorHeap };
    pCommandList-&gt;SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);
    pCommandList-&gt;IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);

    pCommandList-&gt;IASetIndexBuffer(pIndexBufferViewDesc);

    pCommandList-&gt;IASetVertexBuffers(0, 1, pVertexBufferViewDesc);

    pCommandList-&gt;SetGraphicsRootDescriptorTable(0, pCbvSrvDescriptorHeap-&gt;GetGPUDescriptorHandleForHeapStart());
    pCommandList-&gt;SetGraphicsRootDescriptorTable(1, pSamplerDescriptorHeap-&gt;GetGPUDescriptorHandleForHeapStart());

    // Calculate the descriptor offset due to multiple frame resources.
    // 1 SRV + how many CBVs we have currently.
    UINT frameResourceDescriptorOffset = 1 + (frameResourceIndex * m_cityRowCount * m_cityColumnCount);
    CD3DX12_GPU_DESCRIPTOR_HANDLE cbvSrvHandle(pCbvSrvDescriptorHeap-&gt;GetGPUDescriptorHandleForHeapStart(), frameResourceDescriptorOffset, cbvSrvDescriptorSize);

    BOOL usePso1 = TRUE;
    for (UINT i = 0; i &lt; m_cityRowCount; i++)
    {
        for (UINT j = 0; j &lt; m_cityColumnCount; j++)
        {
            // Alternate which PSO to use; the pixel shader is different on 
            // each just as a PSO setting demonstration.
            pCommandList-&gt;SetPipelineState(usePso1 ? pPso1 : pPso2);
            usePso1 = !usePso1;

            // Set this city's CBV table and move to the next descriptor.
            pCommandList-&gt;SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList-&gt;DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

