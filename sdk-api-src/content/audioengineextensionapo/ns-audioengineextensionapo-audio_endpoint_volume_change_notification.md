---
UID: NS:audioengineextensionapo.AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
tech.root: audio
title: AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
ms.date: 06/18/2021
targetos: Windows
description: Represents an audio endpoint volume change APO notification.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
f1_keywords:
 - AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
 - audioengineextensionapo/AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION
dev_langs:
 - c++
---

## -description

Represents an audio endpoint volume change APO notification.

## -struct-fields

### -field endpoint

An [IMMDevice](..//mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint associated with the notification.

### -field volume

A pointer to a [AUDIO_VOLUME_NOTIFICATION_DATA](/windows/win32/api/endpointvolume/ns-endpointvolume-audio_volume_notification_data) representing the new endpoint volume.

## -remarks

## -see-also

