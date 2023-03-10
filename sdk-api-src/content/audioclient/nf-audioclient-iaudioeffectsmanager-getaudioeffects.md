---
UID: NF:audioclient.IAudioEffectsManager.GetAudioEffects
tech.root: CoreAudio
title: IAudioEffectsManager::GetAudioEffects
ms.date: 06/16/2021
targetos: Windows
description: Gets the current list of audio effects for the associated audio stream.
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
 - IAudioEffectsManager::GetAudioEffects
f1_keywords:
 - IAudioEffectsManager::GetAudioEffects
 - audioclient/IAudioEffectsManager::GetAudioEffects
dev_langs:
 - c++
---

## -description

Gets the current list of audio effects for the associated audio stream.

## -parameters

### -param effects

Receives a pointer to an array of [AUDIO_EFFECT](ns-audioclient-audio_effect.md) structures representing the current list of audio effects.

### -param numEffects

Receives the number of **AUDIO_EFFECT** structures returned in *effects*.

## -returns

Returns an HRESULT including but not limited to the following.

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| AUDCLNT_E_DEVICE_INVALIDATED | The associated audio stream has been destroyed. |




## -remarks

The caller is responsible for freeing the array using [CoTaskMemFree](../combaseapi/nf-combaseapi-cotaskmemfree.md).

Register an [IAudioEffectsChangedNotificationClient](nn-audioclient-iaudioeffectschangednotificationclient.md) to receive notifications when the list of audio effects changes.

## -see-also

[AUDIO_EFFECT](ns-audioclient-audio_effect.md)
[IAudioEffectsChangedNotificationClient](nn-audioclient-iaudioeffectschangednotificationclient.md)
