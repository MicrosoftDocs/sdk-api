---
UID: NF:d3d12.ID3D12Device.CreateQueryHeap
title: ID3D12Device::CreateQueryHeap
author: windows-sdk-content
description: Creates a query heap. A query heap contains an array of queries.
old-location: direct3d12\id3d12device_createqueryheap.htm
old-project: direct3d12
ms.assetid: 98B238D0-8E4D-46C1-AC2C-09473A972E71
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: CreateQueryHeap, CreateQueryHeap method, CreateQueryHeap method,ID3D12Device interface, ID3D12Device interface,CreateQueryHeap method, ID3D12Device.CreateQueryHeap, ID3D12Device::CreateQueryHeap, d3d12/ID3D12Device::CreateQueryHeap, direct3d12.id3d12device_createqueryheap
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateQueryHeap
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateQueryHeap


## -description



          Creates a query heap.
          A query heap contains an array of queries.
        


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/1B1CB0D8-B370-4D38-BDA9-21C58D6A8F15">D3D12_QUERY_HEAP_DESC</a>*</b>


            Specifies the query heap in a <a href="https://msdn.microsoft.com/1B1CB0D8-B370-4D38-BDA9-21C58D6A8F15">D3D12_QUERY_HEAP_DESC</a> structure.
          


### -param riid

Type: <b>REFIID</b>


            Specifies a REFIID that uniquely identifies the heap.
          


### -param ppvHeap [out, optional]

Type: <b>void**</b>


            Specifies a pointer to the heap, that will be returned on successful completion of the method.
            <i>ppvHeap</i> can be NULL, to enable capability testing.
            When <i>ppvHeap</i> is NULL, no object will be created and S_FALSE will be returned when <i>pDesc</i> is valid.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




          Refer to <a href="https://msdn.microsoft.com/D7403B5D-7E1B-4DD2-AE45-52E1153233C6">Queries</a> for more information.
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12PredicationQueries</a> sample uses <b>ID3D12Device::CreateQueryHeap</b> as follows:
        

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




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

