---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_MESSAGE
title: DXGI_INFO_QUEUE_MESSAGE (dxgidebug.h)
description: Describes a debug message in the information queue.
helpviewer_keywords: ["DXGI_INFO_QUEUE_MESSAGE","DXGI_INFO_QUEUE_MESSAGE structure [DXGI]","direct3ddxgi.dxgi_info_queue_message","dxgidebug/DXGI_INFO_QUEUE_MESSAGE"]
old-location: direct3ddxgi\dxgi_info_queue_message.htm
tech.root: direct3ddxgi
ms.assetid: F0FF1DC6-8E62-4D35-BCB7-EC3BB314F033
ms.date: 12/05/2018
ms.keywords: DXGI_INFO_QUEUE_MESSAGE, DXGI_INFO_QUEUE_MESSAGE structure [DXGI], direct3ddxgi.dxgi_info_queue_message, dxgidebug/DXGI_INFO_QUEUE_MESSAGE
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_INFO_QUEUE_MESSAGE
 - dxgidebug/DXGI_INFO_QUEUE_MESSAGE
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
 - DXGI_INFO_QUEUE_MESSAGE
---

# DXGI_INFO_QUEUE_MESSAGE structure


## -description

Describes a debug message in the information queue.

## -struct-fields

### -field Producer

A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that produced the message.

### -field Category

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_category">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.

### -field Severity

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.

### -field ID

An integer that uniquely identifies the message.

### -field pDescription

The message string.

### -field DescriptionByteLength

The length of the message string at <b>pDescription</b>, in bytes.

## -remarks

<a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmessage">IDXGIInfoQueue::GetMessage</a> returns a pointer to this structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>