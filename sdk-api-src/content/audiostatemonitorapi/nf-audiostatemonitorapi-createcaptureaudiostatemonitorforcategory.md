---
UID: NF:audiostatemonitorapi.CreateCaptureAudioStateMonitorForCategory
tech.root: CoreAudio
title: CreateCaptureAudioStateMonitorForCategory
ms.date: 06/21/2023
targetos: Windows
description: Creates a new instance of IAudioStateMonitor for the default capture stream for the specified audio category.
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
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - audiostatemonitorapi.h
api_name:
 - CreateCaptureAudioStateMonitorForCategory
f1_keywords:
 - CreateCaptureAudioStateMonitorForCategory
 - audiostatemonitorapi/CreateCaptureAudioStateMonitorForCategory
dev_langs:
 - c++
helpviewer_keywords:
 - CreateCaptureAudioStateMonitorForCategory
---

## -description

Creates a new instance of [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md) for the default capture stream for the specified audio stream category.

## -parameters

### -param category [in]

A member of the [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration specifying the audio stream category for which the audio state monitor is created.

### -param audioStateMonitor [out]

Receives a pointer to the created **IAudioStateMonitor**.

## -returns

Returns an HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK  | Success.    |

## -remarks

## -see-also

