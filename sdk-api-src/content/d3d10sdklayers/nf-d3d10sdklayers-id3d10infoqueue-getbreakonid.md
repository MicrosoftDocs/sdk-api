---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnID
title: ID3D10InfoQueue::GetBreakOnID (d3d10sdklayers.h)
description: Get a message identifier to break on when a message with that identifier passes through the storage filter. (ID3D10InfoQueue.GetBreakOnID)
helpviewer_keywords: ["GetBreakOnID","GetBreakOnID method [Direct3D 10]","GetBreakOnID method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetBreakOnID method","ID3D10InfoQueue.GetBreakOnID","ID3D10InfoQueue::GetBreakOnID","ce099e0a-fe76-1548-a605-708bb35400d4","d3d10sdklayers/ID3D10InfoQueue::GetBreakOnID","direct3d10.id3d10infoqueue_getbreakonid"]
old-location: direct3d10\id3d10infoqueue_getbreakonid.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakonid.htm
ms.date: 12/05/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [Direct3D 10], GetBreakOnID method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnID method, ID3D10InfoQueue.GetBreakOnID, ID3D10InfoQueue::GetBreakOnID, ce099e0a-fe76-1548-a605-708bb35400d4, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnID, direct3d10.id3d10infoqueue_getbreakonid
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
 - ID3D10InfoQueue::GetBreakOnID
 - d3d10sdklayers/ID3D10InfoQueue::GetBreakOnID
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
 - ID3D10InfoQueue.GetBreakOnID
---

# ID3D10InfoQueue::GetBreakOnID


## -description

Get a message identifier to break on when a message with that identifier passes through the storage filter.

## -parameters

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_id">D3D10_MESSAGE_ID</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
