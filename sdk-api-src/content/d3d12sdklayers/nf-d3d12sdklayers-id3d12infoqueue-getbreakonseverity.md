---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetBreakOnSeverity
title: ID3D12InfoQueue::GetBreakOnSeverity (d3d12sdklayers.h)
description: Get a message severity level to break on when a message with that severity level passes through the storage filter. (ID3D12InfoQueue.GetBreakOnSeverity)
helpviewer_keywords: ["GetBreakOnSeverity","GetBreakOnSeverity method","GetBreakOnSeverity method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetBreakOnSeverity method","ID3D12InfoQueue.GetBreakOnSeverity","ID3D12InfoQueue::GetBreakOnSeverity","d3d12sdklayers/ID3D12InfoQueue::GetBreakOnSeverity","direct3d12.id3d12infoqueue_getbreakonseverity"]
old-location: direct3d12\id3d12infoqueue_getbreakonseverity.htm
tech.root: direct3d12
ms.assetid: 255CB074-9C05-4402-9EDE-43AD8C6707E6
ms.date: 12/05/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method, GetBreakOnSeverity method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetBreakOnSeverity method, ID3D12InfoQueue.GetBreakOnSeverity, ID3D12InfoQueue::GetBreakOnSeverity, d3d12sdklayers/ID3D12InfoQueue::GetBreakOnSeverity, direct3d12.id3d12infoqueue_getbreakonseverity
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
 - ID3D12InfoQueue::GetBreakOnSeverity
 - d3d12sdklayers/ID3D12InfoQueue::GetBreakOnSeverity
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
 - ID3D12InfoQueue.GetBreakOnSeverity
---

# ID3D12InfoQueue::GetBreakOnSeverity


## -description

Get a message severity level to break on when a message with that severity level passes through the storage filter.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a></b>

Message severity level to break on.

## -returns

Type: <b>BOOL</b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
