---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnID
title: ID3D11InfoQueue::SetBreakOnID (d3d11sdklayers.h)
description: Set a message identifier to break on when a message with that identifier passes through the storage filter. (ID3D11InfoQueue.SetBreakOnID)
helpviewer_keywords: ["61b0771c-e26b-3275-edc2-79e49d2f26f0","ID3D11InfoQueue interface [Direct3D 11]","SetBreakOnID method","ID3D11InfoQueue.SetBreakOnID","ID3D11InfoQueue::SetBreakOnID","SetBreakOnID","SetBreakOnID method [Direct3D 11]","SetBreakOnID method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::SetBreakOnID","direct3d11.id3d11infoqueue_setbreakonid"]
old-location: direct3d11\id3d11infoqueue_setbreakonid.htm
tech.root: direct3d11
ms.assetid: 7e245c09-bbe1-4601-826b-fe5e71ea6101
ms.date: 12/05/2018
ms.keywords: 61b0771c-e26b-3275-edc2-79e49d2f26f0, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnID method, ID3D11InfoQueue.SetBreakOnID, ID3D11InfoQueue::SetBreakOnID, SetBreakOnID, SetBreakOnID method [Direct3D 11], SetBreakOnID method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnID, direct3d11.id3d11infoqueue_setbreakonid
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
 - ID3D11InfoQueue::SetBreakOnID
 - d3d11sdklayers/ID3D11InfoQueue::SetBreakOnID
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
 - ID3D11InfoQueue.SetBreakOnID
---

# ID3D11InfoQueue::SetBreakOnID


## -description

Set a message identifier to break on when a message with that identifier passes through the storage filter.

## -parameters

### -param ID [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_id">D3D11_MESSAGE_ID</a>).

### -param bEnable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
