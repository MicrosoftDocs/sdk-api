---
UID: NS:audioengineextensionapo.AUDIO_VOLUME_NOTIFICATION_DATA2
tech.root: audio
title: AUDIO_VOLUME_NOTIFICATION_DATA2
ms.date: 02/28/2023
targetos: Windows
description: Represents information about a volume change notification event. This structure is used by the AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2 structure.
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
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA2, *PAUDIO_VOLUME_NOTIFICATION_DATA2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_VOLUME_NOTIFICATION_DATA2
 - PAUDIO_VOLUME_NOTIFICATION_DATA2
f1_keywords:
 - AUDIO_VOLUME_NOTIFICATION_DATA2
 - audioengineextensionapo/AUDIO_VOLUME_NOTIFICATION_DATA2
 - PAUDIO_VOLUME_NOTIFICATION_DATA2
 - audioengineextensionapo/PAUDIO_VOLUME_NOTIFICATION_DATA2
dev_langs:
 - c++
helpviewer_keywords:
 - AUDIO_VOLUME_NOTIFICATION_DATA2
---

## -description

Represents information about a volume change notification event. This structure is used by the [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2](ns-audioengineextensionapo-audio_endpoint_volume_change_notification2.md) structure.

## -struct-fields

### -field notificationData

An [AUDIO_VOLUME_NOTIFICATION_DATA](/windows/win32/api/endpointvolume/ns-endpointvolume-audio_volume_notification_data) structure containing additional information about the volume change event.

### -field masterVolumeInDb

A float value representing the current master volume level of the audio stream in dB.

### -field volumeMinInDb

A float value representing the minimum volume level of the endpoint in decibels. This value remains constant for the lifetime of the audio device specified in the associated [AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-audio_endpoint_volume_apo_notification_descriptor.md). 

### -field volumeMaxInDb

A float value representing the maximum volume level of the endpoint in decibels. This value remains constant for the lifetime of the audio device specified in the associated **AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR**.

### -field volumeIncrementInDb

A float value representing the volume increment of the endpoint in decibels. This value remains constant for the lifetime of the audio device specified in the associated **AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR**.

### -field step

An unsigned integer value representing the current step in the volume range. Is a value in the range from 0 to *stepCount* - 1, where 0 represents the minimum volume level and *stepCount* - 1 represents the maximum level.

### -field stepCount

An unsigned integer value representing the number of steps in the volume range. This value remains constant for the lifetime of the audio device specified in the associated **AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR**.

### -field channelVolumesInDb

The first element in an array of channel volumes in dB. This element contains the current volume level of channel 0 in the audio stream. If the audio stream contains more than one channel, the volume levels for the additional channels immediately follow the **AUDIO_VOLUME_NOTIFICATION_DATA2** structure.

## -remarks

## -see-also
