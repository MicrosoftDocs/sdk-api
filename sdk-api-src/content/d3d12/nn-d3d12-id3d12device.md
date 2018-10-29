---
UID: NN:d3d12.ID3D12Device
title: ID3D12Device
author: windows-sdk-content
description: Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views.
old-location: direct3d12\id3d12device.htm
tech.root: direct3d12
ms.assetid: D32B3397-A1E0-48AF-9251-2EDA96261A9F
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12Device, ID3D12Device interface, ID3D12Device interface,described, d3d12/ID3D12Device, direct3d12.id3d12device
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
 - ID3D12Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device interface


## -description


Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10. Applications targetting Windows 10 should use this interface instead of later versions. Applications targetting a later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface. The latest version of this interface is <a href="https://msdn.microsoft.com/en-us/library/Mt813610(v=VS.85).aspx">ID3D12Device3</a> introduced in Windows 10 Fall Creators Update.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dn788699(v=VS.85).aspx">ID3D12Object</a>. <b>ID3D12Device</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn788653(v=VS.85).aspx">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the features that are supported by the current graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899176(v=VS.85).aspx">CopyDescriptors</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899177(v=VS.85).aspx">CopyDescriptorsSimple</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788655(v=VS.85).aspx">CreateCommandAllocator</a>
</td>
<td align="left" width="63%">
Creates a command allocator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788656(v=VS.85).aspx">CreateCommandList</a>
</td>
<td align="left" width="63%">
Creates a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788657(v=VS.85).aspx">CreateCommandQueue</a>
</td>
<td align="left" width="63%">
Creates a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903827(v=VS.85).aspx">CreateCommandSignature</a>
</td>
<td align="left" width="63%">
This method creates a command signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899178(v=VS.85).aspx">CreateCommittedResource</a>
</td>
<td align="left" width="63%">
Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788658(v=VS.85).aspx">CreateComputePipelineState</a>
</td>
<td align="left" width="63%">
Creates a compute pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788659(v=VS.85).aspx">CreateConstantBufferView</a>
</td>
<td align="left" width="63%">
Creates a constant-buffer view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788661(v=VS.85).aspx">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788662(v=VS.85).aspx">CreateDescriptorHeap</a>
</td>
<td align="left" width="63%">
Creates a descriptor heap object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899179(v=VS.85).aspx">CreateFence</a>
</td>
<td align="left" width="63%">
Creates a fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788663(v=VS.85).aspx">CreateGraphicsPipelineState</a>
</td>
<td align="left" width="63%">
Creates a graphics pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788664(v=VS.85).aspx">CreateHeap</a>
</td>
<td align="left" width="63%">
Creates a heap that can be used with placed resources and reserved resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899180(v=VS.85).aspx">CreatePlacedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is placed in a specific heap.
          Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903828(v=VS.85).aspx">CreateQueryHeap</a>
</td>
<td align="left" width="63%">
Creates a query heap.
          A query heap contains an array of queries.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788668(v=VS.85).aspx">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899181(v=VS.85).aspx">CreateReservedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is reserved, which is not yet mapped to any pages in a heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899182(v=VS.85).aspx">CreateRootSignature</a>
</td>
<td align="left" width="63%">
Creates a root signature layout.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788671(v=VS.85).aspx">CreateSampler</a>
</td>
<td align="left" width="63%">
Create a sampler object that encapsulates sampling information for a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788672(v=VS.85).aspx">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Creates a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899183(v=VS.85).aspx">CreateSharedHandle</a>
</td>
<td align="left" width="63%">
Creates a shared handle to an heap, resource, or fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788674(v=VS.85).aspx">CreateUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Creates a view for unordered accessing.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788676(v=VS.85).aspx">Evict</a>
</td>
<td align="left" width="63%">
Enables the page-out of data, which precludes GPU access of that data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn914411(v=VS.85).aspx">GetAdapterLuid</a>
</td>
<td align="left" width="63%">
Gets a locally unique identifier for the current device (adapter).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn986878(v=VS.85).aspx">GetCopyableFootprints</a>
</td>
<td align="left" width="63%">
Gets a resource layout that can be copied.
          Helps the app fill-in 
          <a href="https://msdn.microsoft.com/en-us/library/Dn986738(v=VS.85).aspx">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and 
          <a href="https://msdn.microsoft.com/en-us/library/Dn986749(v=VS.85).aspx">D3D12_SUBRESOURCE_FOOTPRINT</a> when suballocating space in upload heaps.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt427783(v=VS.85).aspx">GetCustomHeapProperties</a>
</td>
<td align="left" width="63%">
Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899186(v=VS.85).aspx">GetDescriptorHandleIncrementSize</a>
</td>
<td align="left" width="63%">
Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899187(v=VS.85).aspx">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Gets the reason that the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn914412(v=VS.85).aspx">GetNodeCount</a>
</td>
<td align="left" width="63%">
Reports the number of physical adapters (nodes) that are associated with this device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788680(v=VS.85).aspx">GetResourceAllocationInfo</a>
</td>
<td align="left" width="63%">
Gets the size and alignment of memory required for a collection of resources on this adapter.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903829(v=VS.85).aspx">GetResourceTiling</a>
</td>
<td align="left" width="63%">
Gets info about how a tiled resource is broken into tiles.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788682(v=VS.85).aspx">MakeResident</a>
</td>
<td align="left" width="63%">
Makes objects resident for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903831(v=VS.85).aspx">OpenSharedHandle</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903832(v=VS.85).aspx">OpenSharedHandleByName</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn903835(v=VS.85).aspx">SetStablePowerState</a>
</td>
<td align="left" width="63%">
A development-time aid for certain types of profiling and experimental prototyping.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/en-us/library/Dn770336(v=VS.85).aspx">D3D12CreateDevice</a> to create a device. 

For Windows 10 Anniversary some additional functionality is available through <a href="https://msdn.microsoft.com/en-us/library/Mt709132(v=VS.85).aspx">ID3D12Device1</a>.


#### Examples

The <a href="https://msdn.microsoft.com/en-us/library/Mt186624(v=VS.85).aspx">D3D1211on12</a> sample uses <b>ID3D12Device</b> as follows:

Header file declarations.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Pipeline objects.
D3D12_VIEWPORT m_viewport;
ComPtr&lt;IDXGISwapChain3&gt; m_swapChain;
ComPtr&lt;ID3D12Device&gt; m_device;
ComPtr&lt;ID3D12Resource&gt; m_renderTargets[FrameCount];
ComPtr&lt;ID3D12Resource&gt; m_depthStencil;
ComPtr&lt;ID3D12CommandAllocator&gt; m_commandAllocator;
ComPtr&lt;ID3D12GraphicsCommandList&gt; m_commandList;
ComPtr&lt;ID3D12CommandQueue&gt; m_commandQueue;
ComPtr&lt;ID3D12RootSignature &gt;m_rootSignature;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_rtvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_cbvSrvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_dsvHeap;
ComPtr&lt;ID3D12DescriptorHeap&gt; m_samplerHeap;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState1;
ComPtr&lt;ID3D12PipelineState&gt; m_pipelineState2;
D3D12_RECT m_scissorRect;
</pre>
</td>
</tr>
</table></span></div>
Checking supported features.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>inline UINT8 D3D12GetFormatPlaneCount(
    _In_ ID3D12Device* pDevice,
    DXGI_FORMAT Format
    )
{
    D3D12_FEATURE_DATA_FORMAT_INFO formatInfo = {Format};
    if (FAILED(pDevice-&gt;CheckFeatureSupport(D3D12_FEATURE_FORMAT_INFO, &amp;formatInfo, sizeof(formatInfo))))
    {
        return 0;
    }
    return formatInfo.PlaneCount;
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/en-us/library/Dn933255(v=VS.85).aspx">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770457(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859358(v=VS.85).aspx">Creating Descriptors</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709132(v=VS.85).aspx">ID3D12Device1</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt492652(v=VS.85).aspx">ID3D12Device2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn788699(v=VS.85).aspx">ID3D12Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899198(v=VS.85).aspx">Memory Management in Direct3D 12</a>
 

 

