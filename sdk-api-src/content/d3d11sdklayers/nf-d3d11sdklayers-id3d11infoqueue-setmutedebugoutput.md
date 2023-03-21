---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetMuteDebugOutput
title: ID3D11InfoQueue::SetMuteDebugOutput (d3d11sdklayers.h)
description: Set a boolean that turns the debug output on or off. (ID3D11InfoQueue.SetMuteDebugOutput)
helpviewer_keywords: ["845ced1c-0b30-f73c-38de-69cd6425f139","ID3D11InfoQueue interface [Direct3D 11]","SetMuteDebugOutput method","ID3D11InfoQueue.SetMuteDebugOutput","ID3D11InfoQueue::SetMuteDebugOutput","SetMuteDebugOutput","SetMuteDebugOutput method [Direct3D 11]","SetMuteDebugOutput method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::SetMuteDebugOutput","direct3d11.id3d11infoqueue_setmutedebugoutput"]
old-location: direct3d11\id3d11infoqueue_setmutedebugoutput.htm
tech.root: direct3d11
ms.assetid: 0b155d2c-f7b0-4879-8086-8cccbca16a25
ms.date: 12/05/2018
ms.keywords: 845ced1c-0b30-f73c-38de-69cd6425f139, ID3D11InfoQueue interface [Direct3D 11],SetMuteDebugOutput method, ID3D11InfoQueue.SetMuteDebugOutput, ID3D11InfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method [Direct3D 11], SetMuteDebugOutput method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetMuteDebugOutput, direct3d11.id3d11infoqueue_setmutedebugoutput
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
 - ID3D11InfoQueue::SetMuteDebugOutput
 - d3d11sdklayers/ID3D11InfoQueue::SetMuteDebugOutput
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
 - ID3D11InfoQueue.SetMuteDebugOutput
---

# ID3D11InfoQueue::SetMuteDebugOutput


## -description

Set a boolean that turns the debug output on or off.

## -parameters

### -param bMute [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Disable/Enable the debug output (<b>TRUE</b> to disable or mute the output, <b>FALSE</b> to enable the output).

## -remarks

This will stop messages that pass the storage filter from being printed out in the debug output, however those messages will still be added to the message queue.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
