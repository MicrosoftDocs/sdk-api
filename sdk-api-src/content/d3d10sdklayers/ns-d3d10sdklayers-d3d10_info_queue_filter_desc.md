---
UID: NS:d3d10sdklayers.D3D10_INFO_QUEUE_FILTER_DESC
title: D3D10_INFO_QUEUE_FILTER_DESC (d3d10sdklayers.h)
description: Allow or deny certain types of messages to pass through a filter. (D3D10_INFO_QUEUE_FILTER_DESC)
helpviewer_keywords: ["D3D10_INFO_QUEUE_FILTER_DESC","D3D10_INFO_QUEUE_FILTER_DESC structure [Direct3D 10]","c1c85d13-4bf9-82eb-a98e-d91a114dee29","d3d10sdklayers/D3D10_INFO_QUEUE_FILTER_DESC","direct3d10.d3d10_info_queue_filter_desc"]
old-location: direct3d10\d3d10_info_queue_filter_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_info_queue_filter_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_INFO_QUEUE_FILTER_DESC, D3D10_INFO_QUEUE_FILTER_DESC structure [Direct3D 10], c1c85d13-4bf9-82eb-a98e-d91a114dee29, d3d10sdklayers/D3D10_INFO_QUEUE_FILTER_DESC, direct3d10.d3d10_info_queue_filter_desc
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
req.typenames: D3D10_INFO_QUEUE_FILTER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_INFO_QUEUE_FILTER_DESC
 - d3d10sdklayers/D3D10_INFO_QUEUE_FILTER_DESC
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
 - D3D10_INFO_QUEUE_FILTER_DESC
---

# D3D10_INFO_QUEUE_FILTER_DESC structure


## -description

Allow or deny certain types of messages to pass through a filter.

## -struct-fields

### -field NumCategories

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of message categories to allow or deny.

### -field pCategoryList

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a>*</b>

Array of message categories to allow or deny. Array must have at least NumCategories members (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a>).

### -field NumSeverities

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of message severity levels to allow or deny.

### -field pSeverityList

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>*</b>

Array of message severity levels to allow or deny. Array must have at least NumSeverities members (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>).

### -field NumIDs

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of message IDs to allow or deny.

### -field pIDList

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>*</b>

Array of message IDs to allow or deny. Array must have at least NumIDs members (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>).

## -remarks

<b>D3D10_INFO_QUEUE_FILTER_DESC</b> is used to define the allow list and deny list in the <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
