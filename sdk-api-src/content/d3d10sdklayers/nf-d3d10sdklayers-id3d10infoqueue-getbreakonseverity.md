---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnSeverity
title: ID3D10InfoQueue::GetBreakOnSeverity (d3d10sdklayers.h)
description: Get a message severity level to break on when a message with that severity level passes through the storage filter. (ID3D10InfoQueue.GetBreakOnSeverity)
helpviewer_keywords: ["640ea84e-c7af-c3d2-d27b-1edd4a3629f9","GetBreakOnSeverity","GetBreakOnSeverity method [Direct3D 10]","GetBreakOnSeverity method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetBreakOnSeverity method","ID3D10InfoQueue.GetBreakOnSeverity","ID3D10InfoQueue::GetBreakOnSeverity","d3d10sdklayers/ID3D10InfoQueue::GetBreakOnSeverity","direct3d10.id3d10infoqueue_getbreakonseverity"]
old-location: direct3d10\id3d10infoqueue_getbreakonseverity.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakonseverity.htm
ms.date: 12/05/2018
ms.keywords: 640ea84e-c7af-c3d2-d27b-1edd4a3629f9, GetBreakOnSeverity, GetBreakOnSeverity method [Direct3D 10], GetBreakOnSeverity method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnSeverity method, ID3D10InfoQueue.GetBreakOnSeverity, ID3D10InfoQueue::GetBreakOnSeverity, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnSeverity, direct3d10.id3d10infoqueue_getbreakonseverity
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
 - ID3D10InfoQueue::GetBreakOnSeverity
 - d3d10sdklayers/ID3D10InfoQueue::GetBreakOnSeverity
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
 - ID3D10InfoQueue.GetBreakOnSeverity
---

# ID3D10InfoQueue::GetBreakOnSeverity


## -description

Get a message severity level to break on when a message with that severity level passes through the storage filter.

## -parameters

### -param Severity [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
