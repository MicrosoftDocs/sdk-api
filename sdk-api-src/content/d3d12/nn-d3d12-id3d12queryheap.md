---
UID: NN:d3d12.ID3D12QueryHeap
title: ID3D12QueryHeap
author: windows-sdk-content
description: Manages a query heap. A query heap holds an array of queries, referenced by indexes.
old-location: direct3d12\id3d12queryheap.htm
tech.root: direct3d12
ms.assetid: 330DE59A-8098-4255-85DD-0C439DD48250
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12QueryHeap, ID3D12QueryHeap interface, ID3D12QueryHeap interface,described, d3d12/ID3D12QueryHeap, direct3d12.id3d12queryheap
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
 - ID3D12QueryHeap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12QueryHeap interface


## -description


Manages a query heap. A query heap holds an array of queries, referenced by indexes.


## -remarks



For more information, refer to <a href="https://msdn.microsoft.com/D7403B5D-7E1B-4DD2-AE45-52E1153233C6">Queries</a>.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12PredicationQueries</a> sample uses <b>ID3D12QueryHeap</b> as follows:
        

Create a query heap and a query result buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Pipeline objects.
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr&lt;IDXGISwapChain3&gt; m_swapChain;
ComPtr&lt;ID3D12Device&gt; m_device;
ComPtr&lt;ID3D12Resource&gt; m_renderTargets[FrameCount];
ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocators[FrameCount];
ComPtr&lt;ID3D12CommandQueue&gt; m_commandQueue;
ComPtr&lt;ID3D12RootSignature&gt; m_rootSignature;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_rtvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_cbvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_dsvHeap;
ComPtr&lt;ID3D12QueryHeap&gt; m_queryHeap;
UINT m_rtvDescriptorSize;
UINT m_cbvSrvDescriptorSize;
UINT m_frameIndex;

// Synchronization objects.
ComPtr&lt;ID3D12Fence&gt; m_fence;
UINT64 m_fenceValues[FrameCount];
HANDLE m_fenceEvent;

// Asset objects.
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState;
ComPtr&lt;ID3D12PipelineState&gt; m_queryState;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
ComPtr&lt;ID3D12Resource&gt; m_vertexBuffer;
ComPtr&lt;ID3D12Resource&gt; m_constantBuffer;
ComPtr&lt;ID3D12Resource&gt; m_depthStencil;
ComPtr&lt;ID3D12Resource&gt; m_queryResult;
D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Describe and create a heap for occlusion queries.
D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
queryHeapDesc.Count = 1;
queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
ThrowIfFailed(m_device-&gt;CreateQueryHeap(&amp;queryHeapDesc, IID_PPV_ARGS(&amp;m_queryHeap)));
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

