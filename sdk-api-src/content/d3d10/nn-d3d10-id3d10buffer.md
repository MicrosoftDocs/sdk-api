---
UID: NN:d3d10.ID3D10Buffer
title: ID3D10Buffer
author: windows-sdk-content
description: A buffer interface accesses a buffer resource, which is unstructured memory. Buffers typically store vertex or index data.
old-location: direct3d10\id3d10buffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 8a6172fe-deac-4b70-fb31-07255d702e32, ID3D10Buffer, ID3D10Buffer interface [Direct3D 10], ID3D10Buffer interface [Direct3D 10],described, d3d10/ID3D10Buffer, direct3d10.id3d10buffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Buffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Buffer interface


## -description


A buffer interface accesses a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffer resource</a>, which is unstructured memory. Buffers typically store vertex or index data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Buffer</b> interface inherits from <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>. <b>ID3D10Buffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Buffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27420c67-0d3a-46f6-b8ca-2a513a08e21a">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c863ef55-757d-4c0b-ba59-28d30499cf79">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in the resource and deny GPU access to the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6636c07-0e09-4c95-bab3-357ed4ebe0b8">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource retrieved by <a href="https://msdn.microsoft.com/c863ef55-757d-4c0b-ba59-28d30499cf79">ID3D10Buffer::Map</a> and reenable GPU access to the resource.

</td>
</tr>
</table> 


## -remarks



Three types of buffers can be created; <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex</a>, index, and shader-constant buffers. To create a buffer resource, call <a href="https://msdn.microsoft.com/77e943f7-f347-4d04-8e2e-a678d5a2c81c">ID3D10Device::CreateBuffer</a>.

A buffer must be bound to the pipeline before it can be accessed. Buffers can be bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage by calls to <a href="https://msdn.microsoft.com/00fcf32c-982f-4636-bf02-b3f95803684a">ID3D10Device::IASetVertexBuffers</a> and <a href="https://msdn.microsoft.com/2b276345-502e-47fa-9caa-52a82916b577">ID3D10Device::IASetIndexBuffer</a>, and to the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">stream-output</a> stage by a call to <a href="https://msdn.microsoft.com/fd4a71a1-2180-421f-8c9b-735c33f6de75">ID3D10Device::SOSetTargets</a>.

Buffers can be bound to multiple pipeline stages simultaneously for reading. A buffer can also be bound to a single pipeline stage for writing; however, the same buffer cannot be bound for reading and writing simultaneously. For more information, see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">binding resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

