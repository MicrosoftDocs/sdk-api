---
UID: NN:d3d12video.ID3D12VideoDecoderHeap
title: ID3D12VideoDecoderHeap
description: Represents a Direct3D 12 video decoder heap.
tech.root: mf
ms.assetid: b731f246-dbdf-46f4-8ccf-8f59c0f8a26e
ms.date: 05/28/2019
ms.topic: interface
f1_keywords:
- ID3D12VideoDecoderHeap
dev_langs:
- c++
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
topic_type:
- apiref
api_type:
- COM
api_location:
- d3d12video.h
api_name:
- ID3D12VideoDecoderHeap
targetos: Windows
---

# ID3D12VideoDecoderHeap interface

## -description

Represents a Direct3D 12 video decoder heap that contains resolution-dependent resources and state for performing the decode operation.


## -inheritance
ID3D12VideoDecoderHeap interits from ID3D12Pageable. 
## -members

<p>ID3D12VideoDecoderHeap has these methods.</p>
<table>
	<tr>
		<td>Method</td>
		<td>Description</td>
	</tr>
	<tr>
		<td>GetDesc</td>
		<td>TBD</td>
	</tr>
</table>

## -remarks

Get an instance of this class by calling [ID3D12VideoDevice::CreateVideoDecoderHeap](nf-d3d12video-id3d12videodevice-createvideodecoderheap).

## -see-also

[ID3D12VideoDecoderHeap1](nn-d3d12video-id3d12videodecoderheap1)
