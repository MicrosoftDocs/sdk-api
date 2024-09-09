---
UID: NS:audioengineextensionapo.AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
tech.root: audio
title: AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
ms.date: 06/18/2021
targetos: Windows
description: Specifies an endpoint volume APO notification. 
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
req.typenames: AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
f1_keywords:
 - AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
 - audioengineextensionapo/AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR
dev_langs:
 - c++
---

## -description

Specifies an endpoint volume APO notification. 

## -struct-fields

### -field device

The [IMMDevice](../mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint associated with the notification request.


## -remarks

Return an [APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-apo_notification_descriptor.md) containing this structure from an implementation of [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md) to request endpoint volume change APO notifications.

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

