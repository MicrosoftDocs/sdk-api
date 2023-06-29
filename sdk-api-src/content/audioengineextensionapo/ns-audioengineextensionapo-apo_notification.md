---
UID: NS:audioengineextensionapo.APO_NOTIFICATION
tech.root: audio
title: APO_NOTIFICATION
ms.date: 06/19/2021
targetos: Windows
description: Represents a notification for a change to an APO endpoint or system effects.
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
req.typenames: APO_NOTIFICATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - APO_NOTIFICATION
f1_keywords:
 - APO_NOTIFICATION
 - audioengineextensionapo/APO_NOTIFICATION
dev_langs:
 - c++
---

## -description

Represents a notification for a change to an APO endpoint or system effects.

## -struct-fields

### -field type

A value from the [APO_NOTIFICATION_TYPE](ne-audioengineextensionapo-apo_notification_type.md) enumeration specifying the type of change the notification represents.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.audioEndpointVolumeChange

When *type* is APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME, the union value is an [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_endpoint_volume_change_notification.md) representing a notification of a change to APO endpoint volume.

### -field DUMMYUNIONNAME.audioEndpointPropertyChange

When *type* is APO_NOTIFICATION_TYPE_ENDPOINT_PROPERTY_CHANGE, the union value is an  [AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_endpoint_property_change_notification.md) representing a notification of a change to an APO endpoint property.

### -field DUMMYUNIONNAME.audioSystemEffectsPropertyChange

When *type* is APO_NOTIFICATION_TYPE_ENDPOINT_PROPERTY_CHANGE, the union value is an   [AUDIO_SYSTEMEFFECTS_PROPERTY_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_systemeffects_property_change_notification.md) representing a notification of a change to an APO system effect property.

### -field DUMMYUNIONNAME.audioEndpointVolumeChange2

When *type* is APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2, the union value is an   [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2](ns-audioengineextensionapo-audio_endpoint_volume_change_notification2.md) representing a notification of a change to APO endpoint volume that includes master and channel volume, in dB.

### -field DUMMYUNIONNAME.deviceOrientation

When *type* is APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION, the union value is a [DEVICE_ORIENTATION_TYPE](ne-audioengineextensionapo-device_orientation_type.md) representing a device orientation value.

### -field DUMMYUNIONNAME.audioMicrophoneBoostChange

When *type* is APO_NOTIFICATION_TYPE_MICROPHONE_BOOST, the union value is a [AUDIO_MICROPHONE_BOOST_NOTIFICATION](ns-audioengineextensionapo-audio_microphone_boost_apo_notification_descriptor.md) representing an endpoint microphone boost APO notification.

### -field DUMMYUNIONNAME.audioEnvironmentChange

When *type* is APO_NOTIFICATION_TYPE_AUDIO_ENVIRONMENT_STATE_CHANGE, the union value is a [AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_environment_state_change_notification.md) representing an audio environment change APO notification.

## -remarks

Register for the types of notifications you want to receive by implementing [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md). Receive the registered notifications by implementing [IAudioProcessingObjectNotifications::HandleNotification](nf-audioengineextensionapo-iaudioprocessingobjectnotifications-handlenotification.md).


For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

