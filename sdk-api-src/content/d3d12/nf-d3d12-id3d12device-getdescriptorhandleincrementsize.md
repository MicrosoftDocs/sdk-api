---
UID: NF:d3d12.ID3D12Device.GetDescriptorHandleIncrementSize
title: ID3D12Device::GetDescriptorHandleIncrementSize
author: windows-sdk-content
description: Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.
old-location: direct3d12\id3d12device_getdescriptorhandleincrementsize.htm
tech.root: direct3d12
ms.assetid: 4593C153-913A-49DF-ADDC-6FB1E19D3D17
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDescriptorHandleIncrementSize, GetDescriptorHandleIncrementSize method, GetDescriptorHandleIncrementSize method,ID3D12Device interface, ID3D12Device interface,GetDescriptorHandleIncrementSize method, ID3D12Device.GetDescriptorHandleIncrementSize, ID3D12Device::GetDescriptorHandleIncrementSize, d3d12/ID3D12Device::GetDescriptorHandleIncrementSize, direct3d12.id3d12device_getdescriptorhandleincrementsize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12Device.GetDescriptorHandleIncrementSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::GetDescriptorHandleIncrementSize


## -description


Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.


## -parameters




### -param DescriptorHeapType [in]

The <a href="https://msdn.microsoft.com/E74C78BC-B0FC-473A-B4F3-434F50A55E9F">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to get the size of the handle increment for.
          


## -returns



Returns the size of the handle increment for the given type of descriptor heap, including any necessary padding.




## -remarks



The descriptor size returned by this method is used as one input to the helper structures <a href="https://msdn.microsoft.com/91736069-7D13-47B0-B78C-0F6F104F97EB">CD3DX12_CPU_DESCRIPTOR_HANDLE</a> and <a href="https://msdn.microsoft.com/6E405AD6-D370-4B87-849A-C52D64C79BF7">CD3DX12_GPU_DESCRIPTOR_HANDLE</a>.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12PredicationQueries</a> sample uses <b>ID3D12Device::GetDescriptorHandleIncrementSize</b> as follows:
        

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


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

