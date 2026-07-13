---
UID: NF:d3d12.ID3D12Device.CreateDescriptorHeap
title: ID3D12Device::CreateDescriptorHeap (d3d12.h)
description: Creates a descriptor heap object.
helpviewer_keywords: ["CreateDescriptorHeap","CreateDescriptorHeap method","CreateDescriptorHeap method","ID3D12Device interface","ID3D12Device interface","CreateDescriptorHeap method","ID3D12Device.CreateDescriptorHeap","ID3D12Device::CreateDescriptorHeap","d3d12/ID3D12Device::CreateDescriptorHeap","direct3d12.id3d12device_createdescriptorheap"]
old-location: direct3d12\id3d12device_createdescriptorheap.htm
tech.root: direct3d12
ms.assetid: 69EE75CB-7B3D-403D-9798-279A47754ADC
ms.date: 12/05/2018
ms.keywords: CreateDescriptorHeap, CreateDescriptorHeap method, CreateDescriptorHeap method,ID3D12Device interface, ID3D12Device interface,CreateDescriptorHeap method, ID3D12Device.CreateDescriptorHeap, ID3D12Device::CreateDescriptorHeap, d3d12/ID3D12Device::CreateDescriptorHeap, direct3d12.id3d12device_createdescriptorheap
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
 - ID3D12Device::CreateDescriptorHeap
 - d3d12/ID3D12Device::CreateDescriptorHeap
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
 - ID3D12Device.CreateDescriptorHeap
---

# ID3D12Device::CreateDescriptorHeap


## -description

Creates a descriptor heap object.

## -parameters

### -param pDescriptorHeapDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc">D3D12_DESCRIPTOR_HEAP_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc">D3D12_DESCRIPTOR_HEAP_DESC</a> structure that describes the heap.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the descriptor heap interface. See Remarks.
            An input parameter.

### -param ppvHeap [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the descriptor heap.
            <i>ppvHeap</i> can be NULL, to enable capability testing.
            When <i>ppvHeap</i> is NULL, no object will be created and S_FALSE will be returned when <i>pDescriptorHeapDesc</i> is valid.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the descriptor heap object.
              See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the descriptor heap can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap">ID3D12DescriptorHeap</a>) will get the <b>GUID</b> of the interface to a descriptor heap.
      


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12HelloWorld</a> sample uses <b>ID3D12Device::CreateDescriptorHeap</b> as follows:
        

Describe and create a render target view (RTV) descriptor heap.


```cpp
// Create descriptor heaps.
{
    // Describe and create a render target view (RTV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
    rtvHeapDesc.NumDescriptors = FrameCount;
    rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
    rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

    m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
}

// Create frame resources.
{
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

    // Create a RTV for each frame.
    for (UINT n = 0; n < FrameCount; n++)
    {
        ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
        m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
        rtvHandle.Offset(1, m_rtvDescriptorSize);
    }

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>