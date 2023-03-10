---
UID: NN:audioclient.IAudioEffectsChangedNotificationClient
tech.root: CoreAudio
title: IAudioEffectsChangedNotificationClient
ms.date: 06/16/2021
targetos: Windows
description: A callback interface allows applications to receive notifications when the list of audio effects changes or the resources needed to enable an effect changes.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioclient.h
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
 - audioclient.h
api_name:
 - IAudioEffectsChangedNotificationClient
f1_keywords:
 - IAudioEffectsChangedNotificationClient
 - audioclient/IAudioEffectsChangedNotificationClient
dev_langs:
 - c++
---

## -description

A callback interface allows applications to receive notifications when the list of audio effects for the associated audio stream changes or when the resources needed to enable an effect changes, i.e. when the value of the *canSetState* field of the associated [AUDIO_EFFECT](ns-audioclient-audio_effect.md) changes.

## -remarks

Register the callback interface by calling [IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-registeraudioeffectschangednotificationcallback.md).

## -see-also

[AUDIO_EFFECT](ns-audioclient-audio_effect.md)

[IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-registeraudioeffectschangednotificationcallback.md)

