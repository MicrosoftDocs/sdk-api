---
UID: NN:d3d11_3.ID3D11UnorderedAccessView1
title: ID3D11UnorderedAccessView1
author: windows-driver-content
description: An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering.
old-location: direct3d11\id3d11unorderedaccessview1.htm
old-project: direct3d11
ms.assetid: 0D4F7634-0AB1-41C2-8D4F-8C42C1D973D2
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11UnorderedAccessView1, ID3D11UnorderedAccessView1 interface [Direct3D 11], ID3D11UnorderedAccessView1 interface [Direct3D 11], described, d3d11_3/ID3D11UnorderedAccessView1, direct3d11.id3d11unorderedaccessview1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11UnorderedAccessView1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11UnorderedAccessView1 interface


## -description


An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11UnorderedAccessView1</b> interface inherits from <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>. <b>ID3D11UnorderedAccessView1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11UnorderedAccessView1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/277087B3-AAD7-4A6A-91D3-C204B0FA0FE5">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a description of the resource.

</td>
</tr>
</table> 


## -remarks



To create a view for an unordered access resource, call  <a href="https://msdn.microsoft.com/AB64DDED-4C2D-4952-BAA5-3139F973C962">ID3D11Device3::CreateUnorderedAccessView1</a>.

All resources must be bound to the pipeline before they can be accessed. Call <a href="https://msdn.microsoft.com/384a15c0-a035-4f83-a927-e2f763e5fb44">ID3D11DeviceContext::CSSetUnorderedAccessViews</a> to bind an unordered access view to a compute shader; call <a href="https://msdn.microsoft.com/1973d40f-f0d0-497e-be7b-6cf55f8a7da2">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</a> to bind an unordered access view to a pixel shader.




## -see-also




<a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

