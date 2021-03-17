---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddMessage
title: ID3D12InfoQueue::AddMessage (d3d12sdklayers.h)
description: Adds a debug message to the message queue and sends that message to debug output.
helpviewer_keywords: ["AddMessage","AddMessage method","AddMessage method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","AddMessage method","ID3D12InfoQueue.AddMessage","ID3D12InfoQueue::AddMessage","d3d12sdklayers/ID3D12InfoQueue::AddMessage","direct3d12.id3d12infoqueue_addmessage"]
old-location: direct3d12\id3d12infoqueue_addmessage.htm
tech.root: direct3d12
ms.assetid: 34AAF9BB-5340-4DB3-87B9-6C26AB6C881C
ms.date: 12/05/2018
ms.keywords: AddMessage, AddMessage method, AddMessage method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,AddMessage method, ID3D12InfoQueue.AddMessage, ID3D12InfoQueue::AddMessage, d3d12sdklayers/ID3D12InfoQueue::AddMessage, direct3d12.id3d12infoqueue_addmessage
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12InfoQueue::AddMessage
 - d3d12sdklayers/ID3D12InfoQueue::AddMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.AddMessage
---

# ID3D12InfoQueue::AddMessage


## -description

Adds a debug message to the message queue and sends that message to debug output.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category">D3D12_MESSAGE_CATEGORY</a></b>

Category of a message.

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a></b>

Severity of a message.

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id">D3D12_MESSAGE_ID</a></b>

Unique identifier of a message.

### -param pDescription [in]

Type: <b>LPCSTR</b>

User-defined message.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This method is used by the runtime's internal mechanisms to add debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addapplicationmessage">ID3D12InfoQueue::AddApplicationMessage</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>