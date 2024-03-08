---
UID: NE:audioengineextensionapo.APO_NOTIFICATION_TYPE
tech.root: audio
title: APO_NOTIFICATION_TYPE
ms.date: 02/28/2023
targetos: Windows
description: Specifies the type of an APO_NOTIFICATION.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - APO_NOTIFICATION_TYPE
f1_keywords:
 - APO_NOTIFICATION_TYPE
 - audioengineextensionapo/APO_NOTIFICATION_TYPE
dev_langs:
 - c++
---

## -description

Specifies the type of an [APO_NOTIFICATION](ns-audioengineextensionapo-apo_notification.md).

## -enum-fields

### -field APO_NOTIFICATION_TYPE_NONE:0

None.

### -field APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME:1

Endpoint volume notification. The [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_endpoint_volume_change_notification.md) structure conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_ENDPOINT_PROPERTY_CHANGE:2

Endpoint property change notification. The [AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_endpoint_property_change_notification.md) structure conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_SYSTEM_EFFECTS_PROPERTY_CHANGE:3

System effects property change notification.  The [AUDIO_SYSTEMEFFECTS_PROPERTY_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_systemeffects_property_change_notification.md) structure conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2:4

Endpoint volume notification for an endpoint that includes master and channel volume, in dB. The [AUDIO_ENDPOINT_VOLUME_CHANGE_NOTIFICATION2](ns-audioengineextensionapo-audio_endpoint_volume_change_notification2.md) structure conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION:5

Display orientation notification for the device. The [DEVICE_ORIENTATION_TYPE](ne-audioengineextensionapo-device_orientation_type.md) enumeration conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_MICROPHONE_BOOST:6

Microphone boost notification. The [AUDIO_MICROPHONE_BOOST_NOTIFICATION](ns-audioengineextensionapo-audio_microphone_boost_notification.md) structure conveys data for this notification.

### -field APO_NOTIFICATION_TYPE_AUDIO_ENVIRONMENT_STATE_CHANGE

An audio environment state change notification. The [AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION](ns-audioengineextensionapo-audio_environment_state_change_notification.md) structure conveys data for this notification.

## -remarks

Clients use this enumeration to specify requested notification types in their implementations of [IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2](./nf-audioengineextensionapo-iaudioprocessingobjectnotifications2-getaponotificationregistrationinfo2.md) and [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](./nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md). 

The [APO_NOTIFICATION](/windows/win32/api/audioengineextensionapo/ns-audioengineextensionapo-apo_notification) structure passed into [HandleNotification](/windows/win32/api/audioengineextensionapo/nf-audioengineextensionapo-iaudioprocessingobjectnotifications-handlenotification) will contain a different structure in its union field depending on which type of notification is being raised. For more information, see [APO_NOTIFICATION Structure](/windows/win32/api/audioengineextensionapo/ns-audioengineextensionapo-apo_notification).


For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

