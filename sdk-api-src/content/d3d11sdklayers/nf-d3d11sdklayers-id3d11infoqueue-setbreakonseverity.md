---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnSeverity
title: ID3D11InfoQueue::SetBreakOnSeverity (d3d11sdklayers.h)
author: windows-sdk-content
description: Set a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_setbreakonseverity.htm
tech.root: direct3d11
ms.assetid: de977ab5-a277-41fe-a99d-153fa75fc15a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1dc10d17-30bc-4151-6e43-5c1c7fbd518c, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnSeverity method, ID3D11InfoQueue.SetBreakOnSeverity, ID3D11InfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [Direct3D 11], SetBreakOnSeverity method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnSeverity, direct3d11.id3d11infoqueue_setbreakonseverity
ms.topic: method
f1_keywords: 
 - "d3d11sdklayers/ID3D11InfoQueue.SetBreakOnSeverity"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.SetBreakOnSeverity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11InfoQueue::SetBreakOnSeverity


## -description


Set a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_severity">D3D11_MESSAGE_SEVERITY</a>, which represents a message severity level to break on.


### -param bEnable [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
 

 

