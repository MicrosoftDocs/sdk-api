---
UID: NS:d3d11sdklayers.D3D11_INFO_QUEUE_FILTER
title: D3D11_INFO_QUEUE_FILTER (d3d11sdklayers.h)
description: Debug message filter; contains a lists of message types to allow or deny. (D3D11_INFO_QUEUE_FILTER)
helpviewer_keywords: ["9211ecf7-c9cd-c8c2-618a-e4909600a06e","D3D11_INFO_QUEUE_FILTER","D3D11_INFO_QUEUE_FILTER structure [Direct3D 11]","d3d11sdklayers/D3D11_INFO_QUEUE_FILTER","direct3d11.d3d11_info_queue_filter"]
old-location: direct3d11\d3d11_info_queue_filter.htm
tech.root: direct3d11
ms.assetid: 6ff12751-86dd-4ae0-b532-661a70dad21f
ms.date: 12/05/2018
ms.keywords: 9211ecf7-c9cd-c8c2-618a-e4909600a06e, D3D11_INFO_QUEUE_FILTER, D3D11_INFO_QUEUE_FILTER structure [Direct3D 11], d3d11sdklayers/D3D11_INFO_QUEUE_FILTER, direct3d11.d3d11_info_queue_filter
req.header: d3d11sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_INFO_QUEUE_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_INFO_QUEUE_FILTER
 - d3d11sdklayers/D3D11_INFO_QUEUE_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_INFO_QUEUE_FILTER
---

# D3D11_INFO_QUEUE_FILTER structure


## -description

Debug message filter; contains a lists of message types to allow or deny.

## -struct-fields

### -field AllowList

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter_desc">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to allow. See <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter_desc">D3D11_INFO_QUEUE_FILTER_DESC</a>.

### -field DenyList

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter_desc">D3D11_INFO_QUEUE_FILTER_DESC</a></b>

Types of messages that you want to deny.

## -remarks

For use with an <a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-structures">Layer Structures</a>
