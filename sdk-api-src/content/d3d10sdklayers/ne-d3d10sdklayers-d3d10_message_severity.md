---
UID: NE:d3d10sdklayers.D3D10_MESSAGE_SEVERITY
title: D3D10_MESSAGE_SEVERITY (d3d10sdklayers.h)
description: Debug message severity levels for an information queue.
helpviewer_keywords: ["D3D10_MESSAGE_SEVERITY","D3D10_MESSAGE_SEVERITY enumeration [Direct3D 10]","D3D10_MESSAGE_SEVERITY_CORRUPTION","D3D10_MESSAGE_SEVERITY_ERROR","D3D10_MESSAGE_SEVERITY_INFO","D3D10_MESSAGE_SEVERITY_WARNING","b48ff3e8-3124-4d3c-9284-db459579b3d2","d3d10sdklayers/D3D10_MESSAGE_SEVERITY","d3d10sdklayers/D3D10_MESSAGE_SEVERITY_CORRUPTION","d3d10sdklayers/D3D10_MESSAGE_SEVERITY_ERROR","d3d10sdklayers/D3D10_MESSAGE_SEVERITY_INFO","d3d10sdklayers/D3D10_MESSAGE_SEVERITY_WARNING","direct3d10.d3d10_message_severity"]
old-location: direct3d10\d3d10_message_severity.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message_severity.htm
ms.date: 12/05/2018
ms.keywords: D3D10_MESSAGE_SEVERITY, D3D10_MESSAGE_SEVERITY enumeration [Direct3D 10], D3D10_MESSAGE_SEVERITY_CORRUPTION, D3D10_MESSAGE_SEVERITY_ERROR, D3D10_MESSAGE_SEVERITY_INFO, D3D10_MESSAGE_SEVERITY_WARNING, b48ff3e8-3124-4d3c-9284-db459579b3d2, d3d10sdklayers/D3D10_MESSAGE_SEVERITY, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_CORRUPTION, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_ERROR, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_INFO, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_WARNING, direct3d10.d3d10_message_severity
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
req.typenames: D3D10_MESSAGE_SEVERITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MESSAGE_SEVERITY
 - d3d10sdklayers/D3D10_MESSAGE_SEVERITY
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
 - D3D10_MESSAGE_SEVERITY
---

# D3D10_MESSAGE_SEVERITY enumeration


## -description

Debug message severity levels for an information queue.

## -enum-fields

### -field D3D10_MESSAGE_SEVERITY_CORRUPTION:0

Defines some type of corruption which has occurred.

### -field D3D10_MESSAGE_SEVERITY_ERROR

Defines an error message.

### -field D3D10_MESSAGE_SEVERITY_WARNING

Defines a warning message.

### -field D3D10_MESSAGE_SEVERITY_INFO

Defines an information message.

### -field D3D10_MESSAGE_SEVERITY_MESSAGE

## -remarks

Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">D3D10_INFO_QUEUE_FILTER</a>). This API is used by <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage">ID3D10InfoQueue::AddApplicationMessage</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
