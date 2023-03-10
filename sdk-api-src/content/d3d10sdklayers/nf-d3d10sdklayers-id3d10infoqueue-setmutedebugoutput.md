---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetMuteDebugOutput
title: ID3D10InfoQueue::SetMuteDebugOutput (d3d10sdklayers.h)
description: Set a boolean that turns the debug output on or off. (ID3D10InfoQueue.SetMuteDebugOutput)
helpviewer_keywords: ["ID3D10InfoQueue interface [Direct3D 10]","SetMuteDebugOutput method","ID3D10InfoQueue.SetMuteDebugOutput","ID3D10InfoQueue::SetMuteDebugOutput","SetMuteDebugOutput","SetMuteDebugOutput method [Direct3D 10]","SetMuteDebugOutput method [Direct3D 10]","ID3D10InfoQueue interface","d3d10sdklayers/ID3D10InfoQueue::SetMuteDebugOutput","direct3d10.id3d10infoqueue_setmutedebugoutput","fc4951da-744c-9cda-d7ab-407692014dd0"]
old-location: direct3d10\id3d10infoqueue_setmutedebugoutput.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setmutedebugoutput.htm
ms.date: 12/05/2018
ms.keywords: ID3D10InfoQueue interface [Direct3D 10],SetMuteDebugOutput method, ID3D10InfoQueue.SetMuteDebugOutput, ID3D10InfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method [Direct3D 10], SetMuteDebugOutput method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetMuteDebugOutput, direct3d10.id3d10infoqueue_setmutedebugoutput, fc4951da-744c-9cda-d7ab-407692014dd0
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
 - ID3D10InfoQueue::SetMuteDebugOutput
 - d3d10sdklayers/ID3D10InfoQueue::SetMuteDebugOutput
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
 - ID3D10InfoQueue.SetMuteDebugOutput
---

# ID3D10InfoQueue::SetMuteDebugOutput


## -description

Set a boolean that turns the debug output on or off.

## -parameters

### -param bMute [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Disable/Enable the debug output (<b>TRUE</b> to disable or mute the output, <b>FALSE</b> to enable the output).

## -remarks

This will stop messages that pass the storage filter from being printed out in the debug output, however those messages will still be added to the message queue.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
