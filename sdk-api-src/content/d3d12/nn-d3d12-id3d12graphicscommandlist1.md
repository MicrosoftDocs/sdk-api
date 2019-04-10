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
---

# ID3D12GraphicsCommandList1 interface


## -description


Encapsulates a list of graphics commands for rendering, extending the interface to support programmable sample positions, atomic copies for implementing late-latch techniques, and optional depth-bounds testing.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Creators Update, is the latest version of the <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a> interface. Applications targetting Windows 10 Creators Update should use this interface instead of <b>ID3D12GraphicsCommandList</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList1</b> interface inherits from <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>. <b>ID3D12GraphicsCommandList1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/745B641F-B136-46A2-A0EE-F5FDC13656E5">AtomicCopyBufferUINT</a>
</td>
<td align="left" width="63%">
Atomically copies a primary data element of type UINT from one resource to another, along with optional dependent resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F83870E9-5256-4A3E-BAF7-05C4CCB28442">AtomicCopyBufferUINT64</a>
</td>
<td align="left" width="63%">
Atomically copies a primary data element of type UINT64 from one resource to another, along with optional dependent resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/065DBAD3-F4B6-4C94-BA0E-821A46E0B2EE">OMSetDepthBounds</a>
</td>
<td align="left" width="63%">
This method enables you to change the depth bounds dynamically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CF3809C-0EC7-4FBB-AEEF-E74FCD9B836D">ResolveSubresourceRegion</a>
</td>
<td align="left" width="63%">
Copy a region of a multisampled or compressed resource into a non-multisampled or non-compressed resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04627303-20C7-44B1-A62D-45003A13685B">SetSamplePositions</a>
</td>
<td align="left" width="63%">
This method configures the sample positions used by subsequent draw, copy, resolve, and similar operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0AE16797-6F9E-4387-A810-EF59DDC771E6">SetViewInstanceMask</a>
</td>
<td align="left" width="63%">
Set a mask that controls which view instances are enabled for subsequent draws.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

