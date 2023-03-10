---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnID
title: ID3D11InfoQueue::GetBreakOnID (d3d11sdklayers.h)
description: Get a message identifier to break on when a message with that identifier passes through the storage filter. (ID3D11InfoQueue.GetBreakOnID)
helpviewer_keywords: ["GetBreakOnID","GetBreakOnID method [Direct3D 11]","GetBreakOnID method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetBreakOnID method","ID3D11InfoQueue.GetBreakOnID","ID3D11InfoQueue::GetBreakOnID","d3d11sdklayers/ID3D11InfoQueue::GetBreakOnID","dd404ca7-c714-15ae-464b-cc6080192960","direct3d11.id3d11infoqueue_getbreakonid"]
old-location: direct3d11\id3d11infoqueue_getbreakonid.htm
tech.root: direct3d11
ms.assetid: 0efccfd5-55ec-4151-81ca-fe826f44adaa
ms.date: 12/05/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [Direct3D 11], GetBreakOnID method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnID method, ID3D11InfoQueue.GetBreakOnID, ID3D11InfoQueue::GetBreakOnID, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnID, dd404ca7-c714-15ae-464b-cc6080192960, direct3d11.id3d11infoqueue_getbreakonid
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
 - ID3D11InfoQueue::GetBreakOnID
 - d3d11sdklayers/ID3D11InfoQueue::GetBreakOnID
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
 - ID3D11InfoQueue.GetBreakOnID
---

# ID3D11InfoQueue::GetBreakOnID


## -description

Get a message identifier to break on when a message with that identifier passes through the storage filter.

## -parameters

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
