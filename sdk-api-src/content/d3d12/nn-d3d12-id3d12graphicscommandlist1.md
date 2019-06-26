---
UID: NN:d3d12.ID3D12GraphicsCommandList1
title: ID3D12GraphicsCommandList1 (d3d12.h)
author: windows-sdk-content
description: Encapsulates a list of graphics commands for rendering, extending the interface to support programmable sample positions, atomic copies for implementing late-latch techniques, and optional depth-bounds testing.
old-location: direct3d12\id3d12graphicscommandlist1.htm
tech.root: direct3d12
ms.assetid: E156C26B-0E51-4F43-9AB2-373E4C67A496
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList1, ID3D12GraphicsCommandList1 interface, ID3D12GraphicsCommandList1 interface,described, d3d12/ID3D12GraphicsCommandList1, direct3d12.id3d12graphicscommandlist1
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12GraphicsCommandList1"
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
 - ID3D12GraphicsCommandList1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12GraphicsCommandList1 interface


## -description


Encapsulates a list of graphics commands for rendering, extending the interface to support programmable sample positions, atomic copies for implementing late-latch techniques, and optional depth-bounds testing.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Creators Update, is the latest version of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a> interface. Applications targetting Windows 10 Creators Update should use this interface instead of <b>ID3D12GraphicsCommandList</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>. <b>ID3D12GraphicsCommandList1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint">AtomicCopyBufferUINT</a>
</td>
<td align="left" width="63%">
Atomically copies a primary data element of type UINT from one resource to another, along with optional dependent resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64">AtomicCopyBufferUINT64</a>
</td>
<td align="left" width="63%">
Atomically copies a primary data element of type UINT64 from one resource to another, along with optional dependent resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds">OMSetDepthBounds</a>
</td>
<td align="left" width="63%">
This method enables you to change the depth bounds dynamically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion">ResolveSubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region of a multisampled or compressed resource into a non-multisampled or non-compressed resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions">SetSamplePositions</a>
</td>
<td align="left" width="63%">
This method configures the sample positions used by subsequent draw, copy, resolve, and similar operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setviewinstancemask">SetViewInstanceMask</a>
</td>
<td align="left" width="63%">
Set a mask that controls which view instances are enabled for subsequent draws.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
 

 

