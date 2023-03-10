---
UID: NS:d3d11sdklayers.D3D11_MESSAGE
title: D3D11_MESSAGE (d3d11sdklayers.h)
description: A debug message in the Information Queue. (D3D11_MESSAGE)
helpviewer_keywords: ["63ec230f-4005-c7e9-9187-f8c6f44e0780","D3D11_MESSAGE","D3D11_MESSAGE structure [Direct3D 11]","d3d11sdklayers/D3D11_MESSAGE","direct3d11.d3d11_message"]
old-location: direct3d11\d3d11_message.htm
tech.root: direct3d11
ms.assetid: b00a7e61-5394-40bd-bdc1-94da45dfa264
ms.date: 12/05/2018
ms.keywords: 63ec230f-4005-c7e9-9187-f8c6f44e0780, D3D11_MESSAGE, D3D11_MESSAGE structure [Direct3D 11], d3d11sdklayers/D3D11_MESSAGE, direct3d11.d3d11_message
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
req.typenames: D3D11_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_MESSAGE
 - d3d11sdklayers/D3D11_MESSAGE
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
 - D3D11_MESSAGE
---

# D3D11_MESSAGE structure


## -description

A debug message in the Information Queue.

## -struct-fields

### -field Category

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a></b>

The category of the message. See <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a>.

### -field Severity

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a></b>

The severity of the message. See <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a>.

### -field ID

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a></b>

The ID of the message. See <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a>.

### -field pDescription

Type: <b>const char*</b>

The message string.

### -field DescriptionByteLength

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The length of pDescription in bytes.

## -remarks

This structure is returned from <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage">ID3D11InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-structures">Layer Structures</a>
