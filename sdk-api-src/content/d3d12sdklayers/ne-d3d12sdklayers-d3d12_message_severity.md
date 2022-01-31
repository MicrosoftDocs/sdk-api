---
UID: NE:d3d12sdklayers.D3D12_MESSAGE_SEVERITY
title: D3D12_MESSAGE_SEVERITY (d3d12sdklayers.h)
description: Debug message severity levels for an information queue.
helpviewer_keywords: ["D3D12_MESSAGE_SEVERITY","D3D12_MESSAGE_SEVERITY enumeration","D3D12_MESSAGE_SEVERITY_CORRUPTION","D3D12_MESSAGE_SEVERITY_ERROR","D3D12_MESSAGE_SEVERITY_INFO","D3D12_MESSAGE_SEVERITY_MESSAGE","D3D12_MESSAGE_SEVERITY_WARNING","d3d12sdklayers/D3D12_MESSAGE_SEVERITY","d3d12sdklayers/D3D12_MESSAGE_SEVERITY_CORRUPTION","d3d12sdklayers/D3D12_MESSAGE_SEVERITY_ERROR","d3d12sdklayers/D3D12_MESSAGE_SEVERITY_INFO","d3d12sdklayers/D3D12_MESSAGE_SEVERITY_MESSAGE","d3d12sdklayers/D3D12_MESSAGE_SEVERITY_WARNING","direct3d12.d3d12_message_severity"]
old-location: direct3d12\d3d12_message_severity.htm
tech.root: direct3d12
ms.assetid: 44D94C37-4BA8-49FC-BEEF-6666AD59B627
ms.date: 12/05/2018
ms.keywords: D3D12_MESSAGE_SEVERITY, D3D12_MESSAGE_SEVERITY enumeration, D3D12_MESSAGE_SEVERITY_CORRUPTION, D3D12_MESSAGE_SEVERITY_ERROR, D3D12_MESSAGE_SEVERITY_INFO, D3D12_MESSAGE_SEVERITY_MESSAGE, D3D12_MESSAGE_SEVERITY_WARNING, d3d12sdklayers/D3D12_MESSAGE_SEVERITY, d3d12sdklayers/D3D12_MESSAGE_SEVERITY_CORRUPTION, d3d12sdklayers/D3D12_MESSAGE_SEVERITY_ERROR, d3d12sdklayers/D3D12_MESSAGE_SEVERITY_INFO, d3d12sdklayers/D3D12_MESSAGE_SEVERITY_MESSAGE, d3d12sdklayers/D3D12_MESSAGE_SEVERITY_WARNING, direct3d12.d3d12_message_severity
req.header: d3d12sdklayers.h
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
req.typenames: D3D12_MESSAGE_SEVERITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MESSAGE_SEVERITY
 - d3d12sdklayers/D3D12_MESSAGE_SEVERITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_MESSAGE_SEVERITY
---

# D3D12_MESSAGE_SEVERITY enumeration


## -description

Debug message severity levels for an information queue.

## -enum-fields

### -field D3D12_MESSAGE_SEVERITY_CORRUPTION:0

Indicates a corruption error.

### -field D3D12_MESSAGE_SEVERITY_ERROR

Indicates an error.

### -field D3D12_MESSAGE_SEVERITY_WARNING

Indicates a warning.

### -field D3D12_MESSAGE_SEVERITY_INFO

Indicates an information message.

### -field D3D12_MESSAGE_SEVERITY_MESSAGE

Indicates a message other than corruption, error, warning or information.

## -remarks

Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter">D3D12_INFO_QUEUE_FILTER</a>). This API is used by <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addapplicationmessage">AddApplicationMessage</a> and <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage">AddMessage</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>
