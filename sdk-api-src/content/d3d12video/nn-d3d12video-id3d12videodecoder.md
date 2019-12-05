---
UID: NN:d3d12video.ID3D12VideoDecoder
title: ID3D12VideoDecoder
description: Represents a Direct3D 12 video decoder.
tech.root: mf
ms.assetid: 21a497e0-2bc6-4373-b240-bdd7da41fc18
ms.date: 05/28/2019
ms.topic: interface
f1_keywords:
- ID3D12VideoDecoder
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
- ID3D12VideoDecoder
targetos: Windows
---

# ID3D12VideoDecoder interface

## -description

Represents a Direct3D 12 video decoder that contains resolution-independent resources and state for performing the decode operation.


## -inheritance
ID3D12VideoDecoder interits from ID3D12Pageable. 
## -members

<p>ID3D12VideoDecoder has these methods.</p>
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

Get an instance of this class by calling [ID3D12VideoDevice::CreateVideoDecoder](nf-d3d12video-id3d12videodevice-createvideodecoder).

It is not necessary to recreate this object during a resolution change.

## -see-also
