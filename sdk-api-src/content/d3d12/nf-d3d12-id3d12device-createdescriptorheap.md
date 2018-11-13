---
UID: NF:d3d12.ID3D12Device.CreateDescriptorHeap
title: ID3D12Device::CreateDescriptorHeap
author: windows-sdk-content
description: Creates a descriptor heap object.
old-location: direct3d12\id3d12device_createdescriptorheap.htm
tech.root: direct3d12
ms.assetid: 69EE75CB-7B3D-403D-9798-279A47754ADC
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: CreateDescriptorHeap, CreateDescriptorHeap method, CreateDescriptorHeap method,ID3D12Device interface, ID3D12Device interface,CreateDescriptorHeap method, ID3D12Device.CreateDescriptorHeap, ID3D12Device::CreateDescriptorHeap, d3d12/ID3D12Device::CreateDescriptorHeap, direct3d12.id3d12device_createdescriptorheap
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
 - ID3D12Device.CreateDescriptorHeap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateDescriptorHeap


## -description


Creates a descriptor heap object.


## -parameters




### -param pDescriptorHeapDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED">D3D12_DESCRIPTOR_HEAP_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED">D3D12_DESCRIPTOR_HEAP_DESC</a> structure that describes the heap.
          


### -param riid

Type: <b><b>REFIID</b></b>

The globally unique identifier (<b>GUID</b>) for the descriptor heap interface. See Remarks.
            An input parameter.
          


### -param ppvHeap [out]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the descriptor heap.
            <i>ppvHeap</i> can be NULL, to enable capability testing.
            When <i>ppvHeap</i> is NULL, no object will be created and S_FALSE will be returned when <i>pDescriptorHeapDesc</i> is valid.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the descriptor heap object.
              See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
            




## -remarks



The <b>REFIID</b>, or <b>GUID</b>, of the interface to the descriptor heap can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/B6FF011B-3FED-425B-B9D5-A823E6915FD5">ID3D12DescriptorHeap</a>) will get the <b>GUID</b> of the interface to a descriptor heap.
      


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12HelloWorld</a> sample uses <b>ID3D12Device::CreateDescriptorHeap</b> as follows:
        

Describe and create a render target view (RTV) descriptor heap.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create descriptor heaps.
{
    // Describe and create a render target view (RTV) descriptor heap.
    D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
    rtvHeapDesc.NumDescriptors = FrameCount;
    rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
    rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
    ThrowIfFailed(m_device-&gt;CreateDescriptorHeap(&amp;rtvHeapDesc, IID_PPV_ARGS(&amp;m_rtvHeap)));

    m_rtvDescriptorSize = m_device-&gt;GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
}

// Create frame resources.
{
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart());

    // Create a RTV for each frame.
    for (UINT n = 0; n &lt; FrameCount; n++)
    {
        ThrowIfFailed(m_swapChain-&gt;GetBuffer(n, IID_PPV_ARGS(&amp;m_renderTargets[n])));
        m_device-&gt;CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
        rtvHandle.Offset(1, m_rtvDescriptorSize);
    }
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

