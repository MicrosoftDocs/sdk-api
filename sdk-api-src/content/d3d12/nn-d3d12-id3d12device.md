---
UID: NN:d3d12.ID3D12Device
title: ID3D12Device
author: windows-sdk-content
description: Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views.
old-location: direct3d12\id3d12device.htm
tech.root: direct3d12
ms.assetid: D32B3397-A1E0-48AF-9251-2EDA96261A9F
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12Device, ID3D12Device interface, ID3D12Device interface,described, d3d12/ID3D12Device, direct3d12.id3d12device
ms.prod: windows-hardware
ms.technology: windows-devices
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
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10. Applications targetting Windows 10 should use this interface instead of later versions. Applications targetting a later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface. The latest version of this interface is <a href="https://msdn.microsoft.com/038E546C-4000-401A-8A11-7A83F391676E">ID3D12Device3</a> introduced in Windows 10 Fall Creators Update.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device</b> interface inherits from <a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>. <b>ID3D12Device</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the features that are supported by the current graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F995EF34-74FF-4FCA-A018-E2F48DF92450">CopyDescriptors</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6DA1FCDA-042C-4727-9814-B8F57E14CD51">CopyDescriptorsSimple</a>
</td>
<td align="left" width="63%">
Copies descriptors from a source to a destination.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28DA0D59-3DB7-4652-B1EA-3360EA85A659">CreateCommandAllocator</a>
</td>
<td align="left" width="63%">
Creates a command allocator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4C615D7D-6DBC-4EDA-8D72-271EC53047BF">CreateCommandList</a>
</td>
<td align="left" width="63%">
Creates a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/556D068C-9939-4B42-AFC2-4EBB2D7B553B">CreateCommandQueue</a>
</td>
<td align="left" width="63%">
Creates a command queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A44F907-C6E0-4548-A227-84F0CF2EE837">CreateCommandSignature</a>
</td>
<td align="left" width="63%">
This method creates a command signature.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">CreateCommittedResource</a>
</td>
<td align="left" width="63%">
Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57">CreateComputePipelineState</a>
</td>
<td align="left" width="63%">
Creates a compute pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13251F82-4AE9-4234-A0C8-0E666F8A1856">CreateConstantBufferView</a>
</td>
<td align="left" width="63%">
Creates a constant-buffer view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57C0CA35-CFBE-4D79-B8D7-BD01CEBEA144">CreateDepthStencilView</a>
</td>
<td align="left" width="63%">
Creates a depth-stencil view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69EE75CB-7B3D-403D-9798-279A47754ADC">CreateDescriptorHeap</a>
</td>
<td align="left" width="63%">
Creates a descriptor heap object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/731A60CA-644A-4FC2-8461-DDD686363BED">CreateFence</a>
</td>
<td align="left" width="63%">
Creates a fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">CreateGraphicsPipelineState</a>
</td>
<td align="left" width="63%">
Creates a graphics pipeline state object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">CreateHeap</a>
</td>
<td align="left" width="63%">
Creates a heap that can be used with placed resources and reserved resources.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4581A82D-D2B6-4CAE-A336-07B8CF90A0BA">CreatePlacedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is placed in a specific heap.
          Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98B238D0-8E4D-46C1-AC2C-09473A972E71">CreateQueryHeap</a>
</td>
<td align="left" width="63%">
Creates a query heap.
          A query heap contains an array of queries.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4">CreateRenderTargetView</a>
</td>
<td align="left" width="63%">
Creates a render-target view for accessing resource data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">CreateReservedResource</a>
</td>
<td align="left" width="63%">
Creates a resource that is reserved, which is not yet mapped to any pages in a heap.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD3389EC-4086-40F0-B1DB-BCBCF9DDE6BA">CreateRootSignature</a>
</td>
<td align="left" width="63%">
Creates a root signature layout.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/453B2D3D-843E-4DB0-BC47-59BD9C78BFD6">CreateSampler</a>
</td>
<td align="left" width="63%">
Create a sampler object that encapsulates sampling information for a texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4FD7082D-2DA9-469E-BA74-6735D407D5FE">CreateShaderResourceView</a>
</td>
<td align="left" width="63%">
Creates a shader-resource view for accessing data in a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">CreateSharedHandle</a>
</td>
<td align="left" width="63%">
Creates a shared handle to an heap, resource, or fence object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E834E469-2958-44A9-978F-F42D6BB6B1DC">CreateUnorderedAccessView</a>
</td>
<td align="left" width="63%">
Creates a view for unordered accessing.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37F8ABA7-EDA3-4775-8B86-470FC4F95662">Evict</a>
</td>
<td align="left" width="63%">
Enables the page-out of data, which precludes GPU access of that data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/006E72E0-AE09-4834-9ACB-D48698050BF2">GetAdapterLuid</a>
</td>
<td align="left" width="63%">
Gets a locally unique identifier for the current device (adapter).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB3715A9-5A73-45DA-A46F-7889188409A3">GetCopyableFootprints</a>
</td>
<td align="left" width="63%">
Gets a resource layout that can be copied.
          Helps the app fill-in 
          <a href="https://msdn.microsoft.com/74740A52-C2A5-4AF6-92CC-85B5C214423F">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and 
          <a href="https://msdn.microsoft.com/C73B6AB0-F9C5-432E-BA26-3B7772411C95">D3D12_SUBRESOURCE_FOOTPRINT</a> when suballocating space in upload heaps.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD1A7C77-24C3-49D5-8F20-01D5FF7FC895">GetCustomHeapProperties</a>
</td>
<td align="left" width="63%">
Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4593C153-913A-49DF-ADDC-6FB1E19D3D17">GetDescriptorHandleIncrementSize</a>
</td>
<td align="left" width="63%">
Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA723656-BE64-474E-833B-D97576DE0449">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Gets the reason that the device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C5BA618-1B53-45EA-A2E6-19FCAF4FB67C">GetNodeCount</a>
</td>
<td align="left" width="63%">
Reports the number of physical adapters (nodes) that are associated with this device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43467E09-835B-4DB9-B0A4-F75868DE4609">GetResourceAllocationInfo</a>
</td>
<td align="left" width="63%">
Gets the size and alignment of memory required for a collection of resources on this adapter.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32574750-92D3-4CAF-90C6-BA0DEF1E5464">GetResourceTiling</a>
</td>
<td align="left" width="63%">
Gets info about how a tiled resource is broken into tiles.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B3B97DC-5AA3-470E-8EED-3956B295BB94">MakeResident</a>
</td>
<td align="left" width="63%">
Makes objects resident for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F428B06-2906-4ED6-BB75-5DACF2155FA9">OpenSharedHandle</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4866BD8B-31F8-47E0-9228-5F61D6CA2190">OpenSharedHandleByName</a>
</td>
<td align="left" width="63%">
Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6078DAEF-DD8B-4F1F-86C8-96CE7BD691E4">SetStablePowerState</a>
</td>
<td align="left" width="63%">
A development-time aid for certain types of profiling and experimental prototyping.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://msdn.microsoft.com/F403D730-CBD4-4AE0-86F6-8CE122E82CB4">D3D12CreateDevice</a> to create a device. 

For Windows 10 Anniversary some additional functionality is available through <a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D1211on12</a> sample uses <b>ID3D12Device</b> as follows:

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
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/0D360A7C-8A2F-49E1-A5CC-98C958B59D1C">Creating Descriptors</a>



<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>



<a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">ID3D12Device2</a>



<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>



<a href="https://msdn.microsoft.com/94D47EBB-8060-49F6-A1FF-8B7B98AD5363">Memory Management in Direct3D 12</a>
 

 

