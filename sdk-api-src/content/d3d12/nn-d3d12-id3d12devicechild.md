---
UID: NN:d3d12.ID3D12DeviceChild
title: ID3D12DeviceChild (d3d12.h)

description: An interface from which other core interfaces inherit from, including (but not limited to) ID3D12PipelineLibrary, ID3D12CommandList, ID3D12Pageable, and ID3D12RootSignature. It provides a method to get back to the device object it was created against.
old-location: direct3d12\id3d12devicechild.htm
tech.root: direct3d12
ms.assetid: AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A

ms.date: 12/05/2018
ms.keywords: ID3D12DeviceChild, ID3D12DeviceChild interface, ID3D12DeviceChild interface,described, d3d12/ID3D12DeviceChild, direct3d12.id3d12devicechild
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12DeviceChild"
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
 - ID3D12DeviceChild
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DeviceChild interface


## -description


An interface from which other core interfaces inherit from, including (but not limited to) <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary">ID3D12PipelineLibrary</a>,  <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a>. It provides a method to get back to the device object it was created against.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DeviceChild</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>. <b>ID3D12DeviceChild</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DeviceChild</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12devicechild-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Gets a pointer to the device that created this interface. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>
 

 

