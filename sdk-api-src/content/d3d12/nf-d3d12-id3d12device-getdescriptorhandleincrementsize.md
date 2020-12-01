---
UID: NF:d3d12.ID3D12Device.GetDescriptorHandleIncrementSize
title: ID3D12Device::GetDescriptorHandleIncrementSize (d3d12.h)
description: Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.
helpviewer_keywords: ["GetDescriptorHandleIncrementSize","GetDescriptorHandleIncrementSize method","GetDescriptorHandleIncrementSize method","ID3D12Device interface","ID3D12Device interface","GetDescriptorHandleIncrementSize method","ID3D12Device.GetDescriptorHandleIncrementSize","ID3D12Device::GetDescriptorHandleIncrementSize","d3d12/ID3D12Device::GetDescriptorHandleIncrementSize","direct3d12.id3d12device_getdescriptorhandleincrementsize"]
old-location: direct3d12\id3d12device_getdescriptorhandleincrementsize.htm
tech.root: direct3d12
ms.assetid: 4593C153-913A-49DF-ADDC-6FB1E19D3D17
ms.date: 12/05/2018
ms.keywords: GetDescriptorHandleIncrementSize, GetDescriptorHandleIncrementSize method, GetDescriptorHandleIncrementSize method,ID3D12Device interface, ID3D12Device interface,GetDescriptorHandleIncrementSize method, ID3D12Device.GetDescriptorHandleIncrementSize, ID3D12Device::GetDescriptorHandleIncrementSize, d3d12/ID3D12Device::GetDescriptorHandleIncrementSize, direct3d12.id3d12device_getdescriptorhandleincrementsize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::GetDescriptorHandleIncrementSize
 - d3d12/ID3D12Device::GetDescriptorHandleIncrementSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.GetDescriptorHandleIncrementSize
---

# ID3D12Device::GetDescriptorHandleIncrementSize


## -description

Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.

## -parameters

### -param DescriptorHeapType [in]

The <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to get the size of the handle increment for.

## -returns

Returns the size of the handle increment for the given type of descriptor heap, including any necessary padding.

## -remarks

The descriptor size returned by this method is used as one input to the helper structures <a href="/windows/desktop/direct3d12/cd3dx12-cpu-descriptor-handle">CD3DX12_CPU_DESCRIPTOR_HANDLE</a> and <a href="/windows/desktop/direct3d12/cd3dx12-gpu-descriptor-handle">CD3DX12_GPU_DESCRIPTOR_HANDLE</a>.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12PredicationQueries</a> sample uses <b>ID3D12Device::GetDescriptorHandleIncrementSize</b> as follows:
        

Create the descriptor heap for the resources. The <code>m_rtvDescriptorSize</code> variable stores the render target view descriptor handle increment size, and is used in the <b>Create frame resources</b> section of the code.


```cpp
// Create descriptor heaps.
{
    // Describe and create a render target view (RTV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
    rtvHeapDesc.NumDescriptors = FrameCount;
    rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
    rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

    // Describe and create a depth stencil view (DSV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
    dsvHeapDesc.NumDescriptors = 1;
    dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
    dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));

    // Describe and create a constant buffer view (CBV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC cbvHeapDesc = {};
    cbvHeapDesc.NumDescriptors = CbvCountPerFrame * FrameCount;
    cbvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
    cbvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&cbvHeapDesc, IID_PPV_ARGS(&m_cbvHeap)));

    // Describe and create a heap for occlusion queries.
    D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
    queryHeapDesc.Count = 1;
    queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
    ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));

    m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    m_cbvSrvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
}

// Create frame resources.
{
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

    // Create a RTV and a command allocator for each frame.
    for (UINT n = 0; n < FrameCount; n++)
    {
        ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
        m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
        rtvHandle.Offset(1, m_rtvDescriptorSize);

        ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
    }    
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>