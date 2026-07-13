---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetBreakOnID
title: ID3D12InfoQueue::SetBreakOnID (d3d12sdklayers.h)
description: Set a message identifier to break on when a message with that identifier passes through the storage filter. (ID3D12InfoQueue.SetBreakOnID)
helpviewer_keywords: ["ID3D12InfoQueue interface","SetBreakOnID method","ID3D12InfoQueue.SetBreakOnID","ID3D12InfoQueue::SetBreakOnID","SetBreakOnID","SetBreakOnID method","SetBreakOnID method","ID3D12InfoQueue interface","d3d12sdklayers/ID3D12InfoQueue::SetBreakOnID","direct3d12.id3d12infoqueue_setbreakonid"]
old-location: direct3d12\id3d12infoqueue_setbreakonid.htm
tech.root: direct3d12
ms.assetid: 227ECD21-AE8F-41D1-BF56-A516F14BFCD0
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue interface,SetBreakOnID method, ID3D12InfoQueue.SetBreakOnID, ID3D12InfoQueue::SetBreakOnID, SetBreakOnID, SetBreakOnID method, SetBreakOnID method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetBreakOnID, direct3d12.id3d12infoqueue_setbreakonid
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
 - ID3D12InfoQueue::SetBreakOnID
 - d3d12sdklayers/ID3D12InfoQueue::SetBreakOnID
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
 - ID3D12InfoQueue.SetBreakOnID
---

# ID3D12InfoQueue::SetBreakOnID


## -description

Set a message identifier to break on when a message with that identifier passes through the storage filter.

## -parameters

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id">D3D12_MESSAGE_ID</a></b>

Message identifier to break on.

### -param bEnable [in]

Type: <b>BOOL</b>

Turns this breaking condition on or off (true for on, false for off).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
