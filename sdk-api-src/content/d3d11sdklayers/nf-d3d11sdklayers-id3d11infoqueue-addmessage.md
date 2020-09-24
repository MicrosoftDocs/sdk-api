---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddMessage
title: ID3D11InfoQueue::AddMessage (d3d11sdklayers.h)
description: Add a debug message to the message queue and send that message to debug output.
helpviewer_keywords: ["1ac22c4e-5bd3-bec5-0c6b-508a2b311005","AddMessage","AddMessage method [Direct3D 11]","AddMessage method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","AddMessage method","ID3D11InfoQueue.AddMessage","ID3D11InfoQueue::AddMessage","d3d11sdklayers/ID3D11InfoQueue::AddMessage","direct3d11.id3d11infoqueue_addmessage"]
old-location: direct3d11\id3d11infoqueue_addmessage.htm
tech.root: direct3d11
ms.assetid: 7265a273-327a-482b-9d47-6931e031cff8
ms.date: 12/05/2018
ms.keywords: 1ac22c4e-5bd3-bec5-0c6b-508a2b311005, AddMessage, AddMessage method [Direct3D 11], AddMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddMessage method, ID3D11InfoQueue.AddMessage, ID3D11InfoQueue::AddMessage, d3d11sdklayers/ID3D11InfoQueue::AddMessage, direct3d11.id3d11infoqueue_addmessage
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue::AddMessage
 - d3d11sdklayers/ID3D11InfoQueue::AddMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.AddMessage
---

# ID3D11InfoQueue::AddMessage


## -description

Add a debug message to the message queue and send that message to debug output.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a>).

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a>).

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a>).

### -param pDescription [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

User-defined message.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method is used by the runtime's internal mechanisms to add debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addapplicationmessage">ID3D11InfoQueue::AddApplicationMessage</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>