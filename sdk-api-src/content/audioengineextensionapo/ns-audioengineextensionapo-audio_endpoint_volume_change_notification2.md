---
UID: NS:audioengineextensionapo.AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
tech.root: audio
title: AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
ms.date: 02/28/2023
targetos: Windows
description: Represents an audio endpoint volume change APO notification. This is an updated version of AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION that provides additional information in about the volume change event.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
f1_keywords:
 - AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
 - audioengineextensionapo/AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
dev_langs:
 - c++
helpviewer_keywords:
 - AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2
---

## -description

Represents an audio endpoint volume change APO notification. This is an updated version of [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_endpoint_volume_change_notification.md) that provides additional information in about the volume change event.

## -struct-fields

### -field endpoint

An [IMMDevice](..//mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint associated with the notification.

### -field volume

A pointer to a [AUDIO_VOLUME_NOTIFICATION_DATA2](ns-audioengineextensionapo-audio_volume_notification_data2.md) containing information about the volume change event.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

