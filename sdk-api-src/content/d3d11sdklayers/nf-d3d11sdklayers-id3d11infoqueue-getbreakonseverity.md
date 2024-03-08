---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnSeverity
title: ID3D11InfoQueue::GetBreakOnSeverity (d3d11sdklayers.h)
description: Get a message severity level to break on when a message with that severity level passes through the storage filter. (ID3D11InfoQueue.GetBreakOnSeverity)
helpviewer_keywords: ["GetBreakOnSeverity","GetBreakOnSeverity method [Direct3D 11]","GetBreakOnSeverity method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetBreakOnSeverity method","ID3D11InfoQueue.GetBreakOnSeverity","ID3D11InfoQueue::GetBreakOnSeverity","d3d11sdklayers/ID3D11InfoQueue::GetBreakOnSeverity","direct3d11.id3d11infoqueue_getbreakonseverity","feb5cad2-8611-d97c-995e-3501a69206d6"]
old-location: direct3d11\id3d11infoqueue_getbreakonseverity.htm
tech.root: direct3d11
ms.assetid: 4023ddb7-006f-46bc-8be8-34ee2bdd9062
ms.date: 12/05/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method [Direct3D 11], GetBreakOnSeverity method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnSeverity method, ID3D11InfoQueue.GetBreakOnSeverity, ID3D11InfoQueue::GetBreakOnSeverity, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnSeverity, direct3d11.id3d11infoqueue_getbreakonseverity, feb5cad2-8611-d97c-995e-3501a69206d6
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
 - ID3D11InfoQueue::GetBreakOnSeverity
 - d3d11sdklayers/ID3D11InfoQueue::GetBreakOnSeverity
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
 - ID3D11InfoQueue.GetBreakOnSeverity
---

# ID3D11InfoQueue::GetBreakOnSeverity


## -description

Get a message severity level to break on when a message with that severity level passes through the storage filter.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
