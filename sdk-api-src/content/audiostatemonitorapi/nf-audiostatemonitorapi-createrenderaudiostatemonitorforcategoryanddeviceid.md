---
UID: NF:audiostatemonitorapi.CreateRenderAudioStateMonitorForCategoryAndDeviceId
tech.root: CoreAudio
title: CreateRenderAudioStateMonitorForCategoryAndDeviceId
ms.date: 06/21/2023
targetos: Windows
description: Creates a new instance of IAudioStateMonitor for the render streams with the specified audio category and audio device ID.
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
 - CreateRenderAudioStateMonitorForCategoryAndDeviceId
f1_keywords:
 - CreateRenderAudioStateMonitorForCategoryAndDeviceId
 - audiostatemonitorapi/CreateRenderAudioStateMonitorForCategoryAndDeviceId
dev_langs:
 - c++
helpviewer_keywords:
 - CreateRenderAudioStateMonitorForCategoryAndDeviceId
---

## -description

Creates a new instance of [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md) for render streams with the specified audio category and audio device ID.

## -parameters

### -param category [in]

A member of the [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration specifying the audio stream category for which the audio state monitor is created.

### -param deviceId [in]

The unique identifier of the audio device for which the audio state monitor is created. The endpoint may be specified using the MMDevice ID, obtained using [IMMDevice::GetId](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid), or by using its SWD ID, obtained using [Windows.Devices.Enumeration](/uwp/api/windows.devices.enumeration) or [Windows.Media.Devices.MediaDevice](/uwp/api/windows.media.devices.mediadevice).

### -param audioStateMonitor [out]

Receives a pointer to the created **IAudioStateMonitor**.

## -returns

Returns an HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK  | Success.    |

## -remarks

## -see-also

