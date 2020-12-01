---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_FILTER_DESC
title: DXGI_INFO_QUEUE_FILTER_DESC (dxgidebug.h)
description: Describes the types of messages to allow or deny to pass through a filter.
helpviewer_keywords: ["DXGI_INFO_QUEUE_FILTER_DESC","DXGI_INFO_QUEUE_FILTER_DESC structure [DXGI]","direct3ddxgi.dxgi_info_queue_filter_desc","dxgidebug/DXGI_INFO_QUEUE_FILTER_DESC"]
old-location: direct3ddxgi\dxgi_info_queue_filter_desc.htm
tech.root: direct3ddxgi
ms.assetid: B916731B-362B-46AD-BC18-71339A2935B4
ms.date: 12/05/2018
ms.keywords: DXGI_INFO_QUEUE_FILTER_DESC, DXGI_INFO_QUEUE_FILTER_DESC structure [DXGI], direct3ddxgi.dxgi_info_queue_filter_desc, dxgidebug/DXGI_INFO_QUEUE_FILTER_DESC
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
req.typenames: DXGI_INFO_QUEUE_FILTER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_INFO_QUEUE_FILTER_DESC
 - dxgidebug/DXGI_INFO_QUEUE_FILTER_DESC
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
 - DXGI_INFO_QUEUE_FILTER_DESC
---

# DXGI_INFO_QUEUE_FILTER_DESC structure


## -description

Describes the types of messages to allow or deny to pass through a filter.

## -struct-fields

### -field NumCategories

The number of message categories to allow or deny.

### -field pCategoryList

An array of <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_category">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a> enumeration values that describe the message categories to allow or deny. The array must have at least <b>NumCategories</b> number of elements.

### -field NumSeverities

The number of message severity levels to allow or deny.

### -field pSeverityList

An array of <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a> enumeration values that describe the message severity levels to allow or deny. The array must have at least <b>NumSeverities</b> number of elements.

### -field NumIDs

The number of message IDs to allow or deny.

### -field pIDList

An array of integers that represent the message IDs to allow or deny. The array must have at least <b>NumIDs</b> number of elements.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter">DXGI_INFO_QUEUE_FILTER</a> structure.

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>