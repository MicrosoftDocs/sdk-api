---
UID: NF:audioengineextensionapo.IAudioProcessingObjectNotifications.GetApoNotificationRegistrationInfo
tech.root: audio
title: IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo
ms.date: 06/19/2021
targetos: Windows
description: Called by the system to allow clients to register to receive notification callbacks for APO endpoint and system effect notifications.
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
 - IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo
f1_keywords:
 - IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo
 - audioengineextensionapo/IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo
dev_langs:
 - c++
---

## -description

Called by the system to allow clients to register to receive notification callbacks for APO endpoint and system effect notifications. 

## -parameters

### -param apoNotifications [out]

Output parameter that returns a pointer to an array of [APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-apo_notification_descriptor.md) specifying the set of APO changes for which notifications are requested. The callee allocates the APO_NOTIFICATION_DESCRIPTOR structures using [CoTaskMemAlloc](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc); the caller must release the structures by using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when finished.

### -param count [out]

Output parameter specifying the number of items returned in *apoNotifications*.

## -returns

An HRESULT.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

