---
UID: NN:d3d11_3.ID3D11UnorderedAccessView1
title: ID3D11UnorderedAccessView1 (d3d11_3.h)
author: windows-sdk-content
description: An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering.
old-location: direct3d11\id3d11unorderedaccessview1.htm
tech.root: direct3d11
ms.assetid: 0D4F7634-0AB1-41C2-8D4F-8C42C1D973D2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11UnorderedAccessView1, ID3D11UnorderedAccessView1 interface [Direct3D 11], ID3D11UnorderedAccessView1 interface [Direct3D 11],described, d3d11_3/ID3D11UnorderedAccessView1, direct3d11.id3d11unorderedaccessview1
ms.topic: interface
f1_keywords: 
 - "d3d11_3/ID3D11UnorderedAccessView1"
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11UnorderedAccessView1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11UnorderedAccessView1 interface


## -description


An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11UnorderedAccessView1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>. <b>ID3D11UnorderedAccessView1</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11unorderedaccessview1-getdesc1">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a description of the resource.

</td>
</tr>
</table> 


## -remarks



To create a view for an unordered access resource, call  <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createunorderedaccessview1">ID3D11Device3::CreateUnorderedAccessView1</a>.

All resources must be bound to the pipeline before they can be accessed. Call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews">ID3D11DeviceContext::CSSetUnorderedAccessViews</a> to bind an unordered access view to a compute shader; call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</a> to bind an unordered access view to a pixel shader.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

