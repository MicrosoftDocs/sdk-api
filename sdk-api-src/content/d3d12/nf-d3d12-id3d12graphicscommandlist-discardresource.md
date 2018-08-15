---
UID: NF:d3d12.ID3D12GraphicsCommandList.DiscardResource
title: ID3D12GraphicsCommandList::DiscardResource
author: windows-sdk-content
description: Discards a resource.
old-location: direct3d12\id3d12graphicscommandlist_discardresource.htm
old-project: direct3d12
ms.assetid: 2F4DBA5B-F586-4126-8867-BEE650F6D161
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DiscardResource, DiscardResource method, DiscardResource method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,DiscardResource method, ID3D12GraphicsCommandList.DiscardResource, ID3D12GraphicsCommandList::DiscardResource, d3d12/ID3D12GraphicsCommandList::DiscardResource, direct3d12.id3d12graphicscommandlist_discardresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.DiscardResource
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::DiscardResource


## -description


Discards a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> interface for the resource to discard.
            


### -param pRegion [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8F0916CB-3389-40BC-8028-BA8CF9BC566B">D3D12_DISCARD_REGION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/8F0916CB-3389-40BC-8028-BA8CF9BC566B">D3D12_DISCARD_REGION</a> structure that describes details for the discard-resource operation.
            


## -returns



This method does not return a value.
          




## -remarks



The semantics of <b>DiscardResource</b> change based on the command list type.

 For <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE_DIRECT</a>, the following two rules apply:


<ul>
<li>When a resource has the <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET</a> flag, <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RENDER_TARGET</a> resource barrier state.</li>
<li>When a resource has the <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAG _ALLOW_DEPTH_STENCIL</a> flag, <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_DEPTH_WRITE</a>.
</li>
</ul>
For <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE_COMPUTE</a>, the following rule applies:


<ul>
<li>The resource must have the <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS</a> flag, and <b>DiscardResource</b> must be called when the discarded subresource regions are in the <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a> resource barrier state.</li>
</ul>
<b>DiscardResource</b> is not supported on command lists with either <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE_BUNDLE</a> nor <b>D3D12_COMMAND_LIST_TYPE_COPY</b>.




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

