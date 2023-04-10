---
UID: NN:audioengineextensionapo.IAudioProcessingObjectNotifications2
tech.root: audio
title: IAudioProcessingObjectNotifications2
ms.date: 02/28/2023
targetos: Windows
description: Implemented by clients to register for and receive common audio-related notifications for APO endpoint and system effect notifications. This interface adds the ability to determine the notifications types supported on the on the version of Windows running on the current device.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 22621
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectNotifications2
f1_keywords:
 - IAudioProcessingObjectNotifications2
 - audioengineextensionapo/IAudioProcessingObjectNotifications2
dev_langs:
 - c++
helpviewer_keywords:
 - IAudioProcessingObjectNotifications2
---

## -description

Implemented by clients to register for and receive common audio-related notifications for APO endpoint and system effect notifications. This interface provides the method [GetApoNotificationRegistrationInfo2](./nf-audioengineextensionapo-iaudioprocessingobjectnotifications2-getaponotificationregistrationinfo2.md), which has the same behavior as [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](./nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md) with the addition of a parameter that can be used to determine the notifications types supported on the version of Windows running on the current device.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

