---
UID: NN:d3d12sdklayers.ID3D12SharingContract
title: ID3D12SharingContract (d3d12sdklayers.h)
author: windows-sdk-content
description: Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.
old-location: direct3d12\id3d12sharingcontract.htm
tech.root: direct3d12
ms.assetid: 10E61C88-0CDC-42E6-AB70-4911D254C40A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12SharingContract, ID3D12SharingContract interface, ID3D12SharingContract interface,described, d3d12sdklayers/ID3D12SharingContract, direct3d12.id3d12sharingcontract
ms.topic: interface
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
 - ID3D12SharingContract
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12SharingContract interface


## -description


Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools. This interface facilitates diagnostics tools to capture information at a lower level than the DXGI swapchain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12SharingContract</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12SharingContract</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12SharingContract</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12sharingcontract-present">Present</a>
</td>
<td align="left" width="63%">
Shares a resource (or subresource) between the D3D layers and diagnostics tools.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12sharingcontract-sharedfencesignal">SharedFenceSignal</a>
</td>
<td align="left" width="63%">
Signals a shared fence between the D3D layers and diagnostics tools.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

