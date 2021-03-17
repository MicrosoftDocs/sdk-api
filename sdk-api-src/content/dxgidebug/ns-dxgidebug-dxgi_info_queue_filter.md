---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_FILTER
title: DXGI_INFO_QUEUE_FILTER (dxgidebug.h)
description: Describes a debug message filter, which contains lists of message types to allow and deny.
helpviewer_keywords: ["DXGI_INFO_QUEUE_FILTER","DXGI_INFO_QUEUE_FILTER structure [DXGI]","direct3ddxgi.dxgi_info_queue_filter","dxgidebug/DXGI_INFO_QUEUE_FILTER"]
old-location: direct3ddxgi\dxgi_info_queue_filter.htm
tech.root: direct3ddxgi
ms.assetid: 95E68ECE-39D2-4D16-9A8F-FE6E527A83E3
ms.date: 12/05/2018
ms.keywords: DXGI_INFO_QUEUE_FILTER, DXGI_INFO_QUEUE_FILTER structure [DXGI], direct3ddxgi.dxgi_info_queue_filter, dxgidebug/DXGI_INFO_QUEUE_FILTER
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_INFO_QUEUE_FILTER
 - dxgidebug/DXGI_INFO_QUEUE_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_INFO_QUEUE_FILTER
---

# DXGI_INFO_QUEUE_FILTER structure


## -description

Describes a debug message filter, which contains lists of message types to allow and deny.

## -struct-fields

### -field AllowList

A <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter_desc">DXGI_INFO_QUEUE_FILTER_DESC</a> structure that describes the types of messages to allow.

### -field DenyList

A <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter_desc">DXGI_INFO_QUEUE_FILTER_DESC</a> structure that describes the types of messages to deny.

## -remarks

Use with an <a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a> interface.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>