---
UID: NF:audioclient.IAudioEffectsManager.RegisterAudioEffectsChangedNotificationCallback
tech.root: CoreAudio
title: IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback
ms.date: 06/16/2021
targetos: Windows
description: Registers an AudioEffectsChangedNotificationClient interface.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioclient.h
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
 - audioclient.h
api_name:
 - IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback
f1_keywords:
 - IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback
 - audioclient/IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback
dev_langs:
 - c++
---

## -description

Registers an [IAudioEffectsChangedNotificationClient](nn-audioclient-iaudioeffectschangednotificationclient.md) interface. This callback interface allows applications to receive notifications when the list of audio effects changes or the resources needed to enable an effect changes, i.e. when the value of the *canSetState* field of the associated [AUDIO_EFFECT](ns-audioclient-audio_effect.md) changes.

## -parameters

### -param client

The **IAudioEffectsChangedNotificationClient** interface to register.

## -returns

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| AUDCLNT_E_DEVICE_INVALIDATED | The associated audio stream has been destroyed. |

## -remarks

Unregister the callback interface by calling [UnregisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-unregisteraudioeffectschangednotificationcallback.md).

## -see-also

