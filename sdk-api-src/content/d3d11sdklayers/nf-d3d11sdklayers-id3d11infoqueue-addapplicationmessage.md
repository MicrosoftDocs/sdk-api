---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddApplicationMessage
title: ID3D11InfoQueue::AddApplicationMessage (d3d11sdklayers.h)
description: Add a user-defined message to the message queue and send that message to debug output. (ID3D11InfoQueue.AddApplicationMessage)
helpviewer_keywords: ["566d6299-a5dc-568a-e71a-3c990b282e93","AddApplicationMessage","AddApplicationMessage method [Direct3D 11]","AddApplicationMessage method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","AddApplicationMessage method","ID3D11InfoQueue.AddApplicationMessage","ID3D11InfoQueue::AddApplicationMessage","d3d11sdklayers/ID3D11InfoQueue::AddApplicationMessage","direct3d11.id3d11infoqueue_addapplicationmessage"]
old-location: direct3d11\id3d11infoqueue_addapplicationmessage.htm
tech.root: direct3d11
ms.assetid: ca5a5e33-f912-4283-8b23-b212ace6089c
ms.date: 12/05/2018
ms.keywords: 566d6299-a5dc-568a-e71a-3c990b282e93, AddApplicationMessage, AddApplicationMessage method [Direct3D 11], AddApplicationMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddApplicationMessage method, ID3D11InfoQueue.AddApplicationMessage, ID3D11InfoQueue::AddApplicationMessage, d3d11sdklayers/ID3D11InfoQueue::AddApplicationMessage, direct3d11.id3d11infoqueue_addapplicationmessage
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
 - ID3D11InfoQueue::AddApplicationMessage
 - d3d11sdklayers/ID3D11InfoQueue::AddApplicationMessage
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
 - ID3D11InfoQueue.AddApplicationMessage
---

# ID3D11InfoQueue::AddApplicationMessage


## -description

Add a user-defined message to the message queue and send that message to debug output.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a>).

### -param pDescription [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Message string.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
