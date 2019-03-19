---
UID: NN:d3d11.ID3D11UnorderedAccessView
title: ID3D11UnorderedAccessView (d3d11.h)
author: windows-sdk-content
description: A view interface specifies the parts of a resource the pipeline can access during rendering.
old-location: direct3d11\id3d11unorderedaccessview.htm
tech.root: direct3d11
ms.assetid: 9def4a7d-f145-4073-8d7d-bf3c7ac7a060
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 0d091716-fdf1-7aff-5a05-68258dd1f745, ID3D11UnorderedAccessView, ID3D11UnorderedAccessView interface [Direct3D 11], ID3D11UnorderedAccessView interface [Direct3D 11],described, d3d11/ID3D11UnorderedAccessView, direct3d11.id3d11unorderedaccessview
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11UnorderedAccessView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11UnorderedAccessView interface


## -description


A view interface specifies the parts of a resource the pipeline can access during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11UnorderedAccessView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11UnorderedAccessView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11UnorderedAccessView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5174d08a-f631-4e48-94af-c53d03d7e2f8">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the resource.

</td>
</tr>
</table> 


## -remarks



To create a view for an unordered access resource, call  <a href="https://msdn.microsoft.com/85b85114-4e3f-407e-879c-ef4c120cb3c1">ID3D11Device::CreateUnorderedAccessView</a>.

All resources must be bound to the pipeline before they can be accessed. Call <a href="https://msdn.microsoft.com/384a15c0-a035-4f83-a927-e2f763e5fb44">ID3D11DeviceContext::CSSetUnorderedAccessViews</a> to bind an unordered access view to a compute shader; call <a href="https://msdn.microsoft.com/1973d40f-f0d0-497e-be7b-6cf55f8a7da2">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</a> to bind an unordered access view to a pixel shader.




## -see-also




<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

