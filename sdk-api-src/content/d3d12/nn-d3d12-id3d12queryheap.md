---
UID: NN:d3d12.ID3D12QueryHeap
title: ID3D12QueryHeap (d3d12.h)
description: Manages a query heap. A query heap holds an array of queries, referenced by indexes.
helpviewer_keywords: ["ID3D12QueryHeap","ID3D12QueryHeap interface","ID3D12QueryHeap interface","described","d3d12/ID3D12QueryHeap","direct3d12.id3d12queryheap"]
old-location: direct3d12\id3d12queryheap.htm
tech.root: direct3d12
ms.assetid: 330DE59A-8098-4255-85DD-0C439DD48250
ms.date: 12/05/2018
ms.keywords: ID3D12QueryHeap, ID3D12QueryHeap interface, ID3D12QueryHeap interface,described, d3d12/ID3D12QueryHeap, direct3d12.id3d12queryheap
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
 - ID3D12QueryHeap
 - d3d12/ID3D12QueryHeap
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
 - ID3D12QueryHeap
---

# ID3D12QueryHeap interface


## -description

Manages a query heap. A query heap holds an array of queries, referenced by indexes.

## -remarks

For more information, refer to <a href="/windows/desktop/direct3d12/queries">Queries</a>.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12PredicationQueries</a> sample uses <b>ID3D12QueryHeap</b> as follows:
        

Create a query heap and a query result buffer.


```cpp
// Pipeline objects.
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocators[FrameCount];
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12DescriptorHeap> m_cbvHeap;
ComPtr<ID3D12DescriptorHeap> m_dsvHeap;
ComPtr<ID3D12QueryHeap> m_queryHeap;
UINT m_rtvDescriptorSize;
UINT m_cbvSrvDescriptorSize;
UINT m_frameIndex;

// Synchronization objects.
ComPtr<ID3D12Fence> m_fence;
UINT64 m_fenceValues[FrameCount];
HANDLE m_fenceEvent;

// Asset objects.
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12PipelineState> m_queryState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
ComPtr<ID3D12Resource> m_vertexBuffer;
ComPtr<ID3D12Resource> m_constantBuffer;
ComPtr<ID3D12Resource> m_depthStencil;
ComPtr<ID3D12Resource> m_queryResult;
D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

```

```cpp
// Describe and create a heap for occlusion queries.
D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
queryHeapDesc.Count = 1;
queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>