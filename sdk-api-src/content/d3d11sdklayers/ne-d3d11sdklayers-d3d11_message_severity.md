---
UID: NE:d3d11sdklayers.D3D11_MESSAGE_SEVERITY
title: D3D11_MESSAGE_SEVERITY (d3d11sdklayers.h)
description: Debug message severity levels for an information queue.
helpviewer_keywords: ["5817bf39-bfcb-e96c-175e-08c952303b59","D3D11_MESSAGE_SEVERITY","D3D11_MESSAGE_SEVERITY enumeration [Direct3D 11]","D3D11_MESSAGE_SEVERITY_CORRUPTION","D3D11_MESSAGE_SEVERITY_ERROR","D3D11_MESSAGE_SEVERITY_INFO","D3D11_MESSAGE_SEVERITY_MESSAGE","D3D11_MESSAGE_SEVERITY_WARNING","d3d11sdklayers/D3D11_MESSAGE_SEVERITY","d3d11sdklayers/D3D11_MESSAGE_SEVERITY_CORRUPTION","d3d11sdklayers/D3D11_MESSAGE_SEVERITY_ERROR","d3d11sdklayers/D3D11_MESSAGE_SEVERITY_INFO","d3d11sdklayers/D3D11_MESSAGE_SEVERITY_MESSAGE","d3d11sdklayers/D3D11_MESSAGE_SEVERITY_WARNING","direct3d11.d3d11_message_severity"]
old-location: direct3d11\d3d11_message_severity.htm
tech.root: direct3d11
ms.assetid: 63143187-8e16-4ba4-aec5-8530ed31accb
ms.date: 12/05/2018
ms.keywords: 5817bf39-bfcb-e96c-175e-08c952303b59, D3D11_MESSAGE_SEVERITY, D3D11_MESSAGE_SEVERITY enumeration [Direct3D 11], D3D11_MESSAGE_SEVERITY_CORRUPTION, D3D11_MESSAGE_SEVERITY_ERROR, D3D11_MESSAGE_SEVERITY_INFO, D3D11_MESSAGE_SEVERITY_MESSAGE, D3D11_MESSAGE_SEVERITY_WARNING, d3d11sdklayers/D3D11_MESSAGE_SEVERITY, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_CORRUPTION, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_ERROR, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_INFO, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_MESSAGE, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_WARNING, direct3d11.d3d11_message_severity
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
req.typenames: D3D11_MESSAGE_SEVERITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_MESSAGE_SEVERITY
 - d3d11sdklayers/D3D11_MESSAGE_SEVERITY
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
 - D3D11_MESSAGE_SEVERITY
---

# D3D11_MESSAGE_SEVERITY enumeration


## -description

Debug message severity levels for an information queue.

## -enum-fields

### -field D3D11_MESSAGE_SEVERITY_CORRUPTION:0

Defines some type of corruption which has occurred.

### -field D3D11_MESSAGE_SEVERITY_ERROR

Defines an error message.

### -field D3D11_MESSAGE_SEVERITY_WARNING

Defines a warning message.

### -field D3D11_MESSAGE_SEVERITY_INFO

Defines an information message.

### -field D3D11_MESSAGE_SEVERITY_MESSAGE

Defines a message other than corruption, error, warning, or information.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

## -remarks

Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">D3D11_INFO_QUEUE_FILTER</a>). This API is used by <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addapplicationmessage">ID3D11InfoQueue::AddApplicationMessage</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-enums">Layer Enumerations</a>
