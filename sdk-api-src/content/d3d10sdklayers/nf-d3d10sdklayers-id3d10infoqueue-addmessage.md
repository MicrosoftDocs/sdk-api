---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddMessage
title: ID3D10InfoQueue::AddMessage (d3d10sdklayers.h)
description: Add a Direct3D 10 debug message to the message queue and send that message to debug output.
helpviewer_keywords: ["AddMessage","AddMessage method [Direct3D 10]","AddMessage method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","AddMessage method","ID3D10InfoQueue.AddMessage","ID3D10InfoQueue::AddMessage","cdfe0171-65a2-02d0-bad5-e630bf30db83","d3d10sdklayers/ID3D10InfoQueue::AddMessage","direct3d10.id3d10infoqueue_addmessage"]
old-location: direct3d10\id3d10infoqueue_addmessage.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addmessage.htm
ms.date: 12/05/2018
ms.keywords: AddMessage, AddMessage method [Direct3D 10], AddMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddMessage method, ID3D10InfoQueue.AddMessage, ID3D10InfoQueue::AddMessage, cdfe0171-65a2-02d0-bad5-e630bf30db83, d3d10sdklayers/ID3D10InfoQueue::AddMessage, direct3d10.id3d10infoqueue_addmessage
req.header: d3d10sdklayers.h
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
 - ID3D10InfoQueue::AddMessage
 - d3d10sdklayers/ID3D10InfoQueue::AddMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.AddMessage
---

# ID3D10InfoQueue::AddMessage


## -description

Add a Direct3D 10 debug message to the message queue and send that message to debug output.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a>).

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>).

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>).

### -param pDescription [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

User-defined message.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method is used by the runtime's internal mechanisms to add Direct3D 10 debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage">ID3D10InfoQueue::AddApplicationMessage</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>