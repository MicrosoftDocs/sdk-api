---
UID: NN:d3d11.ID3D11Buffer
title: ID3D11Buffer (d3d11.h)
author: windows-sdk-content
description: A buffer interface accesses a buffer resource, which is unstructured memory. Buffers typically store vertex or index data.
old-location: direct3d11\id3d11buffer.htm
tech.root: direct3d11
ms.assetid: 7224de57-75cb-4d68-9d70-f5dd2f92b1fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 12286442-1fa2-0c8c-14c5-6c9af4348aee, ID3D11Buffer, ID3D11Buffer interface [Direct3D 11], ID3D11Buffer interface [Direct3D 11],described, d3d11/ID3D11Buffer, direct3d11.id3d11buffer
ms.topic: interface
f1_keywords: 
 - "d3d11/ID3D11Buffer"
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
 - ID3D11Buffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Buffer interface


## -description


A buffer interface accesses a buffer resource, which is unstructured memory. Buffers typically store vertex or index data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Buffer</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>. <b>ID3D11Buffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Buffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11buffer-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a buffer resource.

</td>
</tr>
</table> 


## -remarks



There are three types of buffers: vertex, index, or a shader-constant buffer. Create a buffer resource by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createbuffer">ID3D11Device::CreateBuffer</a>.

A buffer must be bound to the pipeline before it can be accessed. Buffers can be bound to the input-assembler stage by calls to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers">ID3D11DeviceContext::IASetVertexBuffers</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetindexbuffer">ID3D11DeviceContext::IASetIndexBuffer</a>, to the stream-output stage by a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sosettargets">ID3D11DeviceContext::SOSetTargets</a>, and to a shader stage by calling the appropriate shader method (such as <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers">ID3D11DeviceContext::VSSetConstantBuffers</a> for example).

Buffers can be bound to multiple pipeline stages simultaneously for reading. A buffer can also be bound to a single pipeline stage for writing; however, the same buffer cannot be bound for reading and writing simultaneously.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

