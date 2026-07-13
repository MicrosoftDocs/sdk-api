---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddApplicationMessage
title: ID3D10InfoQueue::AddApplicationMessage (d3d10sdklayers.h)
description: Add a user-defined message to the message queue and send that message to debug output. (ID3D10InfoQueue.AddApplicationMessage)
helpviewer_keywords: ["1d152bbb-d6ef-f0f3-d61f-2156408503ce","AddApplicationMessage","AddApplicationMessage method [Direct3D 10]","AddApplicationMessage method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","AddApplicationMessage method","ID3D10InfoQueue.AddApplicationMessage","ID3D10InfoQueue::AddApplicationMessage","d3d10sdklayers/ID3D10InfoQueue::AddApplicationMessage","direct3d10.id3d10infoqueue_addapplicationmessage"]
old-location: direct3d10\id3d10infoqueue_addapplicationmessage.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addapplicationmessage.htm
ms.date: 12/05/2018
ms.keywords: 1d152bbb-d6ef-f0f3-d61f-2156408503ce, AddApplicationMessage, AddApplicationMessage method [Direct3D 10], AddApplicationMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddApplicationMessage method, ID3D10InfoQueue.AddApplicationMessage, ID3D10InfoQueue::AddApplicationMessage, d3d10sdklayers/ID3D10InfoQueue::AddApplicationMessage, direct3d10.id3d10infoqueue_addapplicationmessage
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
 - ID3D10InfoQueue::AddApplicationMessage
 - d3d10sdklayers/ID3D10InfoQueue::AddApplicationMessage
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
 - ID3D10InfoQueue.AddApplicationMessage
---

# ID3D10InfoQueue::AddApplicationMessage


## -description

Add a user-defined message to the message queue and send that message to debug output.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>).

### -param pDescription [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Message string.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
