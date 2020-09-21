---
UID: NN:d3d10.ID3D10Buffer
title: ID3D10Buffer (d3d10.h)
description: A buffer interface accesses a buffer resource, which is unstructured memory. Buffers typically store vertex or index data.
helpviewer_keywords: ["8a6172fe-deac-4b70-fb31-07255d702e32","ID3D10Buffer","ID3D10Buffer interface [Direct3D 10]","ID3D10Buffer interface [Direct3D 10]","described","d3d10/ID3D10Buffer","direct3d10.id3d10buffer"]
old-location: direct3d10\id3d10buffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer.htm
ms.date: 12/05/2018
ms.keywords: 8a6172fe-deac-4b70-fb31-07255d702e32, ID3D10Buffer, ID3D10Buffer interface [Direct3D 10], ID3D10Buffer interface [Direct3D 10],described, d3d10/ID3D10Buffer, direct3d10.id3d10buffer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Buffer
 - d3d10/ID3D10Buffer
dev_langs:
 - c++
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
---

# ID3D10Buffer interface


## -description

A buffer interface accesses a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer resource</a>, which is unstructured memory. Buffers typically store vertex or index data.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Buffer</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>. <b>ID3D10Buffer</b> also has these types of members:
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
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a buffer resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-map">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in the resource and deny GPU access to the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-unmap">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the resource retrieved by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-map">ID3D10Buffer::Map</a> and reenable GPU access to the resource.

</td>
</tr>
</table>

## -remarks

Three types of buffers can be created; <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">vertex</a>, index, and shader-constant buffers. To create a buffer resource, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createbuffer">ID3D10Device::CreateBuffer</a>.

A buffer must be bound to the pipeline before it can be accessed. Buffers can be bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage by calls to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetvertexbuffers">ID3D10Device::IASetVertexBuffers</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetindexbuffer">ID3D10Device::IASetIndexBuffer</a>, and to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">stream-output</a> stage by a call to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-sosettargets">ID3D10Device::SOSetTargets</a>.

Buffers can be bound to multiple pipeline stages simultaneously for reading. A buffer can also be bound to a single pipeline stage for writing; however, the same buffer cannot be bound for reading and writing simultaneously. For more information, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">binding resources</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>