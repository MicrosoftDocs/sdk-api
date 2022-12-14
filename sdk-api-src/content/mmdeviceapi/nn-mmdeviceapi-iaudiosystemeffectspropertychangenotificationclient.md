---
UID: NN:mmdeviceapi.IAudioSystemEffectsPropertyChangeNotificationClient
tech.root: audio
title: IAudioSystemEffectsPropertyChangeNotificationClient
ms.date: 06/18/2021
targetos: Windows
description: A callback interface implemented by clients to receive notifications when audio system effect properties change.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mmdeviceapi.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IAudioSystemEffectsPropertyChangeNotificationClient
f1_keywords:
 - IAudioSystemEffectsPropertyChangeNotificationClient
 - mmdeviceapi/IAudioSystemEffectsPropertyChangeNotificationClient
dev_langs:
 - c++
---

## -description

A callback interface implemented by clients to receive notifications when audio system effect properties change.

## -remarks

Register the interface to receive callbacks by calling [IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification](nf-mmdeviceapi-iaudiosystemeffectspropertystore-registerpropertychangenotification.md). Unregister the callback interface by calling [IAudioSystemEffectsPropertyStore::UnregisterPropertyChangeNotification](nf-mmdeviceapi-iaudiosystemeffectspropertystore-unregisterpropertychangenotification.md).

## -see-also

