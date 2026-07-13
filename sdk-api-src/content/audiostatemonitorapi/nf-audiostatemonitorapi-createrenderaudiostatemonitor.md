---
UID: NF:audiostatemonitorapi.CreateRenderAudioStateMonitor
tech.root: CoreAudio
title: CreateRenderAudioStateMonitor
ms.date: 06/21/2023
targetos: Windows
description: Creates a new instance of IAudioStateMonitor for render streams.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audiostatemonitorapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: windows.media.mediacontrol.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 19043
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audiostatemonitorapi.h
api_name:
 - CreateRenderAudioStateMonitor
f1_keywords:
 - CreateRenderAudioStateMonitor
 - audiostatemonitorapi/CreateRenderAudioStateMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - CreateRenderAudioStateMonitor
---

## -description

Creates a new instance of [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md) for render streams.

## -parameters

### -param audioStateMonitor [out]

Receives a pointer to the created **IAudioStateMonitor**.

## -returns

Returns an HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK  | Success.    |

## -remarks

## -see-also

