---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetBreakOnSeverity
title: ID3D10InfoQueue::SetBreakOnSeverity (d3d10sdklayers.h)
author: windows-sdk-content
description: Set a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_setbreakonseverity.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setbreakonseverity.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10InfoQueue interface [Direct3D 10],SetBreakOnSeverity method, ID3D10InfoQueue.SetBreakOnSeverity, ID3D10InfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [Direct3D 10], SetBreakOnSeverity method [Direct3D 10],ID3D10InfoQueue interface, a333f38c-3dea-80fe-c7bb-b11dfec7e140, d3d10sdklayers/ID3D10InfoQueue::SetBreakOnSeverity, direct3d10.id3d10infoqueue_setbreakonseverity
ms.topic: method
f1_keywords: ["d3d10sdklayers/ID3D10InfoQueue.SetBreakOnSeverity"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.SetBreakOnSeverity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10InfoQueue::SetBreakOnSeverity


## -description


Set a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_severity">D3D10_MESSAGE_SEVERITY</a>).


### -param bEnable [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
 

 

