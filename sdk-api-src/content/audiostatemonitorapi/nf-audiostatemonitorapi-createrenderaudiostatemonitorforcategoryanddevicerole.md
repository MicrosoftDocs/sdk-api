---
UID: NF:audiostatemonitorapi.CreateRenderAudioStateMonitorForCategoryAndDeviceRole
tech.root: CoreAudio
title: CreateRenderAudioStateMonitorForCategoryAndDeviceRole
ms.date: 06/21/2023
targetos: Windows
description: Creates a new instance of IAudioStateMonitor for render streams with the specified audio category and audio device role.
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
 - CreateRenderAudioStateMonitorForCategoryAndDeviceRole
f1_keywords:
 - CreateRenderAudioStateMonitorForCategoryAndDeviceRole
 - audiostatemonitorapi/CreateRenderAudioStateMonitorForCategoryAndDeviceRole
dev_langs:
 - c++
helpviewer_keywords:
 - CreateRenderAudioStateMonitorForCategoryAndDeviceRole
---

## -description

Creates a new instance of [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md) for render streams with the specified audio category and audio device role.

## -parameters

### -param category [in]

A member of the [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration specifying the audio stream category for which the audio state monitor is created.

### -param role [in]

A member of the [ERole](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration specifying the audio device role for which the audio state monitor is created.

### -param audioStateMonitor [out]

Receives a pointer to the created **IAudioStateMonitor**.

## -returns

Returns an HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK  | Success.    |

## -remarks

## -see-also

