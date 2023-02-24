---
UID: NF:audioengineextensionapo.IAudioProcessingObjectNotifications.HandleNotification
tech.root: audio
title: IAudioProcessingObjectNotifications::HandleNotification
ms.date: 06/19/2021
targetos: Windows
description: Called by the system to notify clients of changes to APO endpoints or system effects.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectNotifications::HandleNotification
f1_keywords:
 - IAudioProcessingObjectNotifications::HandleNotification
 - audioengineextensionapo/IAudioProcessingObjectNotifications::HandleNotification
dev_langs:
 - c++
---

## -description

Called by the system to notify clients of changes to APO endpoints or system effects.

## -parameters

### -param apoNotification

An [APO_NOTIFICATION](ns-audioengineextensionapo-apo_notification.md) representing the APO change associated with the notification.

## -remarks

 Specify the set of APO changes for which this method is called by implementing [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md).


This method will be called after [LockForProcess](/windows/win32/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectconfiguration-lockforprocess) is called and will stop being called before [UnlockForProcess](/windows/win32/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectconfiguration-unlockforprocess). If there are any notifications in flight, they might get executed during or after **UnlockForProcess**. The APO must handle synchronization in this case.

> [!NOTE]
> APOs must query each property once to get its initial value because **HandleNotification** method is only invoked when any of the properties have changed. The exceptions to this are the initial audio endpoint volume when the APO registers for APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME and the value of PKEY_AudioEndpoint_Disable_SysFx if the APO registers for APO_NOTIFICATION_TYPE_ENDPOINT_PROPERTY_CHANGE


For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).


## -see-also

