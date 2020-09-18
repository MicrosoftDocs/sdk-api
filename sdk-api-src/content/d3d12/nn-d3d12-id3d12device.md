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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>. <b>ID3D12Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the features that are supported by the current graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors">CopyDescriptors</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple">CopyDescriptorsSimple</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator">CreateCommandAllocator</a>
</td>
<td align="left" width="63%">
Creates a command allocator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandlist">CreateCommandList</a>
</td>
<td align="left" width="63%">
Creates a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue">CreateCommandQueue</a>
</td>
<td align="left" width="63%">
Creates a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature">CreateCommandSignature</a>
</td>
<td align="left" width="63%">
This method creates a command signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">CreateCommittedResource</a>
</td>
<td align="left" width="63%">
Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate">CreateComputePipelineState</a>
</td>
<td align="left" width="63%">
Creates a compute pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview">CreateConstantBufferView</a>
</td>
<td align="left" width="63%">
Creates a constant-buffer view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap">CreateDescriptorHeap</a>
</td>
<td align="left" width="63%">
Creates a descriptor heap object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createfence">CreateFence</a>
</td>
<td align="left" width="63%">
Creates a fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate">CreateGraphicsPipelineState</a>
</td>
<td align="left" width="63%">
Creates a graphics pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">CreateHeap</a>
</td>
<td align="left" width="63%">
Creates a heap that can be used with placed resources and reserved resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is placed in a specific heap.
          Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap">CreateQueryHeap</a>
</td>
<td align="left" width="63%">
Creates a query heap.
          A query heap contains an array of queries.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is reserved, which is not yet mapped to any pages in a heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">CreateRootSignature</a>
</td>
<td align="left" width="63%">
Creates a root signature layout.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler">CreateSampler</a>
</td>
<td align="left" width="63%">
Create a sampler object that encapsulates sampling information for a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Creates a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsharedhandle">CreateSharedHandle</a>
</td>
<td align="left" width="63%">
Creates a shared handle to an heap, resource, or fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview">CreateUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Creates a view for unordered accessing.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict">Evict</a>
</td>
<td align="left" width="63%">
Enables the page-out of data, which precludes GPU access of that data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getadapterluid">GetAdapterLuid</a>
</td>
<td align="left" width="63%">
Gets a locally unique identifier for the current device (adapter).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints">GetCopyableFootprints</a>
</td>
<td align="left" width="63%">
Gets a resource layout that can be copied.
          Helps the app fill-in 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint">D3D12_SUBRESOURCE_FOOTPRINT</a> when suballocating space in upload heaps.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties">GetCustomHeapProperties</a>
</td>
<td align="left" width="63%">
Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize">GetDescriptorHandleIncrementSize</a>
</td>
<td align="left" width="63%">
Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Gets the reason that the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getnodecount">GetNodeCount</a>
</td>
<td align="left" width="63%">
Reports the number of physical adapters (nodes) that are associated with this device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo">GetResourceAllocationInfo</a>
</td>
<td align="left" width="63%">
Gets the size and alignment of memory required for a collection of resources on this adapter.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling">GetResourceTiling</a>
</td>
<td align="left" width="63%">
Gets info about how a tiled resource is broken into tiles.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-makeresident">MakeResident</a>
</td>
<td align="left" width="63%">
Makes objects resident for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-opensharedhandle">OpenSharedHandle</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname">OpenSharedHandleByName</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate">SetStablePowerState</a>
</td>
<td align="left" width="63%">
A development-time aid for certain types of profiling and experimental prototyping.

</td>
</tr>
</table>

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