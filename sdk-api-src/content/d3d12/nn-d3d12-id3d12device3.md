---
UID: NN:d3d12.ID3D12Device3
title: ID3D12Device3 (d3d12.h)
description: Represents a virtual adapter. This interface extends ID3D12Device2 to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
old-location: direct3d12\id3d12device3.htm
tech.root: direct3d12
ms.assetid: 038E546C-4000-401A-8A11-7A83F391676E
ms.date: 12/05/2018
ms.keywords: ID3D12Device3, ID3D12Device3 interface, ID3D12Device3 interface,described, d3d12/ID3D12Device3, direct3d12.id3d12device3
f1_keywords:
- d3d12/ID3D12Device3
dev_langs:
- c++
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3d12.dll
api_name:
- ID3D12Device3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device3 interface


## -description


Represents a virtual adapter. This interface extends <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a> to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Fall Creators Update, is the latest version of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> interface. Applications targeting the Windows 10 Fall Creators Update and later should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>. <b>ID3D12Device3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Device3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident">EnqueueMakeResident</a>
</td>
<td align="left" width="63%">
Asynchronously makes objects resident for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress">OpenExistingHeapFromAddress</a>
</td>
<td align="left" width="63%">
Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/mt813613(v=vs.85)">OpenExistingHeapFromFileMapping</a>
</td>
<td align="left" width="63%">
Creates a special-purpose diagnostic heap in system memory from a file mapping handle. The created heap can persist even in the event of a GPU-fault or device-removed scenario.

</td>
</tr>
</table> 


## -remarks



Use <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice">D3D12CreateDevice</a> to create a device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>
 

 

