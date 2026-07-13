---
UID: NN:d3d12.ID3D12Device
title: ID3D12Device (d3d12.h)
description: Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views.
helpviewer_keywords: ["ID3D12Device","ID3D12Device interface","ID3D12Device interface","described","d3d12/ID3D12Device","direct3d12.id3d12device"]
old-location: direct3d12\id3d12device.htm
tech.root: direct3d12
ms.assetid: D32B3397-A1E0-48AF-9251-2EDA96261A9F
ms.date: 12/05/2018
ms.keywords: ID3D12Device, ID3D12Device interface, ID3D12Device interface,described, d3d12/ID3D12Device, direct3d12.id3d12device
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
 - ID3D12Device
 - d3d12/ID3D12Device
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
 - ID3D12Device
---

# ID3D12Device interface


## -description

Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10. Applications targetting Windows 10 should use this interface instead of later versions. Applications targetting a later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface. The latest version of this interface is <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device3">ID3D12Device3</a> introduced in Windows 10 Fall Creators Update.</div><div> </div>

## -inheritance

The <b>ID3D12Device</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>. <b>ID3D12Device</b> also has these types of members:

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice">D3D12CreateDevice</a> to create a device. 

For Windows 10 Anniversary some additional functionality is available through <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>.


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D1211on12</a> sample uses <b>ID3D12Device</b> as follows:

Header file declarations.


```cpp
// Pipeline objects.
D3D12_VIEWPORT m_viewport;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12Resource> m_depthStencil;
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature >m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12DescriptorHeap> m_cbvSrvHeap;
ComPtr<ID3D12DescriptorHeap> m_dsvHeap;
ComPtr<ID3D12DescriptorHeap> m_samplerHeap;
ComPtr<ID3D12PipelineState> m_pipelineState1;
ComPtr<ID3D12PipelineState> m_pipelineState2;
D3D12_RECT m_scissorRect;

```


Checking supported features.


```cpp
inline UINT8 D3D12GetFormatPlaneCount(
    _In_ ID3D12Device* pDevice,
    DXGI_FORMAT Format
    )
{
    D3D12_FEATURE_DATA_FORMAT_INFO formatInfo = {Format};
    if (FAILED(pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_INFO, &formatInfo, sizeof(formatInfo))))
    {
        return 0;
    }
    return formatInfo.PlaneCount;
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/direct3d12/creating-descriptors">Creating Descriptors</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>



<a href="/windows/desktop/direct3d12/memory-management">Memory Management in Direct3D 12</a>
