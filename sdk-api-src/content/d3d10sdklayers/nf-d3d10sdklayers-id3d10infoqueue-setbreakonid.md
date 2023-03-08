---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetBreakOnID
title: ID3D10InfoQueue::SetBreakOnID (d3d10sdklayers.h)
description: Set a message identifier to break on when a message with that identifier passes through the storage filter. (ID3D10InfoQueue.SetBreakOnID)
helpviewer_keywords: ["ID3D10InfoQueue interface [Direct3D 10]","SetBreakOnID method","ID3D10InfoQueue.SetBreakOnID","ID3D10InfoQueue::SetBreakOnID","SetBreakOnID","SetBreakOnID method [Direct3D 10]","SetBreakOnID method [Direct3D 10]","ID3D10InfoQueue interface","d3d10sdklayers/ID3D10InfoQueue::SetBreakOnID","d9deed23-ec78-a913-c2b7-8c24e15d1e45","direct3d10.id3d10infoqueue_setbreakonid"]
old-location: direct3d10\id3d10infoqueue_setbreakonid.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setbreakonid.htm
ms.date: 12/05/2018
ms.keywords: ID3D10InfoQueue interface [Direct3D 10],SetBreakOnID method, ID3D10InfoQueue.SetBreakOnID, ID3D10InfoQueue::SetBreakOnID, SetBreakOnID, SetBreakOnID method [Direct3D 10], SetBreakOnID method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetBreakOnID, d9deed23-ec78-a913-c2b7-8c24e15d1e45, direct3d10.id3d10infoqueue_setbreakonid
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
 - ID3D10InfoQueue::SetBreakOnID
 - d3d10sdklayers/ID3D10InfoQueue::SetBreakOnID
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
 - ID3D10InfoQueue.SetBreakOnID
---

# ID3D10InfoQueue::SetBreakOnID


## -description

Set a message identifier to break on when a message with that identifier passes through the storage filter.

## -parameters

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>).

### -param bEnable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
