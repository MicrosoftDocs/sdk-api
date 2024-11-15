---
UID: NS:audioengineextensionapo.APO_NOTIFICATION_DESCRIPTOR
tech.root: audio
title: APO_NOTIFICATION_DESCRIPTOR
ms.date: 06/18/2021
targetos: Windows
description: Specifies a requested APO notification.
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
req.typenames: APO_NOTIFICATION_DESCRIPTOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - APO_NOTIFICATION_DESCRIPTOR
f1_keywords:
 - APO_NOTIFICATION_DESCRIPTOR
 - audioengineextensionapo/APO_NOTIFICATION_DESCRIPTOR
dev_langs:
 - c++
---

## -description

Specifies a requested APO notification.

## -struct-fields

### -field type

A value from the [APO_NOTIFICATION_TYPE](ne-audioengineextensionapo-apo_notification_type.md) enumeration

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.audioEndpointVolume

An [AUDIO_ENDPOINT_VOLUME_APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-audio_endpoint_volume_apo_notification_descriptor.md) specifying an endpoint volume change APO notification.

### -field DUMMYUNIONNAME.audioEndpointPropertyChange

An [AUDIO_ENDPOINT_PROPERTY_CHANGE_APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-audio_endpoint_property_change_apo_notification_descriptor.md) specifying an endpoint property change APO notification.

### -field DUMMYUNIONNAME.audioSystemEffectsPropertyChange

An [AUDIO_SYSTEMEFFECTS_PROPERTY_CHANGE_APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-audio_systemeffects_property_change_apo_notification_descriptor.md)  specifying a system effects property change APO notification.

### -field DUMMYUNIONNAME.audioMicrophoneBoost

An [AUDIO_MICROPHONE_BOOST_APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-audio_microphone_boost_apo_notification_descriptor.md) specifying a microphone boost APO notifications.


## -remarks

Return this structure from an implementation of [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md) or [IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2](nf-audioengineextensionapo-iaudioprocessingobjectnotifications2-getaponotificationregistrationinfo2.md) to specify a requested APO notifications.

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

