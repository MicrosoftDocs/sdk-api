---
UID: NF:mmdeviceapi.IAudioSystemEffectsPropertyStore.RegisterPropertyChangeNotification
tech.root: audio
title: IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification
ms.date: 06/18/2021
targetos: Windows
description: Registers an IAudioSystemEffectsPropertyChangeNotificationClient callback interface to receive notifications when audio system effect properties change.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mmdeviceapi.h
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
 - mmdeviceapi.h
api_name:
 - IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification
f1_keywords:
 - IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification
 - mmdeviceapi/IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification
dev_langs:
 - c++
---

## -description

Registers an [IAudioSystemEffectsPropertyChangeNotificationClient](nn-mmdeviceapi-iaudiosystemeffectspropertychangenotificationclient.md) callback interface to receive notifications when audio system effect properties change.

## -parameters

### -param callback

A pointer to the **IAudioSystemEffectsPropertyChangeNotificationClient** callback interface to register.

## -returns

Returns S_OK on success.

## -remarks

This method should not be used by APOs and should only be used by hardware support apps to register for notifications.

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

