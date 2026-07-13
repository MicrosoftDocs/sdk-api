---
UID: NS:d3d10sdklayers.D3D10_INFO_QUEUE_FILTER
title: D3D10_INFO_QUEUE_FILTER (d3d10sdklayers.h)
description: Debug message filter; contains a lists of message types to allow or deny. (D3D10_INFO_QUEUE_FILTER)
helpviewer_keywords: ["9c94d10b-2b6f-b70e-75d1-72a61687e2b9","D3D10_INFO_QUEUE_FILTER","D3D10_INFO_QUEUE_FILTER structure [Direct3D 10]","d3d10sdklayers/D3D10_INFO_QUEUE_FILTER","direct3d10.d3d10_info_queue_filter"]
old-location: direct3d10\d3d10_info_queue_filter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_info_queue_filter.htm
ms.date: 12/05/2018
ms.keywords: 9c94d10b-2b6f-b70e-75d1-72a61687e2b9, D3D10_INFO_QUEUE_FILTER, D3D10_INFO_QUEUE_FILTER structure [Direct3D 10], d3d10sdklayers/D3D10_INFO_QUEUE_FILTER, direct3d10.d3d10_info_queue_filter
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
req.typenames: D3D10_INFO_QUEUE_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_INFO_QUEUE_FILTER
 - d3d10sdklayers/D3D10_INFO_QUEUE_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10sdklayers.h
api_name:
 - D3D10_INFO_QUEUE_FILTER
---

# D3D10_INFO_QUEUE_FILTER structure


## -description

Debug message filter; contains a lists of message types to allow or deny.

## -struct-fields

### -field AllowList

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should allow.

### -field DenyList

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should reject.

## -remarks

For use with an <a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>.

Providing an allow list with non-zero values causes only the specified combination of categories, severities and message IDs to be allowed.  
      Messages that do not match the specified combination will be rejected.

Providing a deny list with non-zero values causes the specified combination of categories, severities and message IDs to be rejected.
      Messages that do not match the specified combination will be allowed.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
