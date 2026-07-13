---
UID: NS:d3d10sdklayers.D3D10_MESSAGE
title: D3D10_MESSAGE (d3d10sdklayers.h)
description: A debug message in the Information Queue. (D3D10_MESSAGE)
helpviewer_keywords: ["3d6907d3-259d-0e6a-db64-2a00690f975d","D3D10_MESSAGE","D3D10_MESSAGE structure [Direct3D 10]","d3d10sdklayers/D3D10_MESSAGE","direct3d10.d3d10_message"]
old-location: direct3d10\d3d10_message.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message.htm
ms.date: 12/05/2018
ms.keywords: 3d6907d3-259d-0e6a-db64-2a00690f975d, D3D10_MESSAGE, D3D10_MESSAGE structure [Direct3D 10], d3d10sdklayers/D3D10_MESSAGE, direct3d10.d3d10_message
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
req.typenames: D3D10_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MESSAGE
 - d3d10sdklayers/D3D10_MESSAGE
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
 - D3D10_MESSAGE
---

# D3D10_MESSAGE structure


## -description

A debug message in the Information Queue.

## -struct-fields

### -field Category

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a></b>

The category of the message. See <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a>.

### -field Severity

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a></b>

The severity of the message. See <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>.

### -field ID

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a></b>

The ID of the message. See <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>.

### -field pDescription

Type: <b>const char*</b>

The message string.

### -field DescriptionByteLength

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The length of pDescription in bytes.

## -remarks

This structure is returned from <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage">ID3D10InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
