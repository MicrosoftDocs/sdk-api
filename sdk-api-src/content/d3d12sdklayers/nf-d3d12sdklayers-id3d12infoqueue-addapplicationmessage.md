---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.AddApplicationMessage
title: ID3D12InfoQueue::AddApplicationMessage (d3d12sdklayers.h)
description: Adds a user-defined message to the message queue and sends that message to debug output.
helpviewer_keywords: ["AddApplicationMessage","AddApplicationMessage method","AddApplicationMessage method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","AddApplicationMessage method","ID3D12InfoQueue.AddApplicationMessage","ID3D12InfoQueue::AddApplicationMessage","d3d12sdklayers/ID3D12InfoQueue::AddApplicationMessage","direct3d12.id3d12infoqueue_addapplicationmessage"]
old-location: direct3d12\id3d12infoqueue_addapplicationmessage.htm
tech.root: direct3d12
ms.assetid: C5979BF4-C44D-461F-8FAB-D0577691C5BF
ms.date: 12/05/2018
ms.keywords: AddApplicationMessage, AddApplicationMessage method, AddApplicationMessage method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,AddApplicationMessage method, ID3D12InfoQueue.AddApplicationMessage, ID3D12InfoQueue::AddApplicationMessage, d3d12sdklayers/ID3D12InfoQueue::AddApplicationMessage, direct3d12.id3d12infoqueue_addapplicationmessage
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
 - ID3D12InfoQueue::AddApplicationMessage
 - d3d12sdklayers/ID3D12InfoQueue::AddApplicationMessage
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
 - ID3D12InfoQueue.AddApplicationMessage
---

# ID3D12InfoQueue::AddApplicationMessage


## -description

Adds a user-defined message to the message queue and sends that message to debug output.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a></b>

Severity of a message.

### -param pDescription [in]

Type: <b>LPCSTR</b>

Specifies the message string.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>