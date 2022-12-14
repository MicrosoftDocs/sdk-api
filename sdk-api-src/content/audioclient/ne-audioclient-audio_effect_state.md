---
UID: NE:audioclient.AUDIO_EFFECT_STATE
tech.root: CoreAudio
title: AUDIO_EFFECT_STATE
ms.date: 06/16/2021
targetos: Windows
description: Specifies the state of an audio effect.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioclient.h
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
 - audioclient.h
api_name:
 - AUDIO_EFFECT_STATE
f1_keywords:
 - AUDIO_EFFECT_STATE
 - audioclient/AUDIO_EFFECT_STATE
dev_langs:
 - c++
---

## -description

Specifies the state of an audio effect.

## -enum-fields

### -field AUDIO_EFFECT_STATE_OFF

The audio effect is off.

### -field AUDIO_EFFECT_STATE_ON

The audio effect is on.

## -remarks

Get the state of an audio effect by calling [IAudioEffectsManager::GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md) and checking the *state* field of the returned [AUDIO_EFFECT](ns-audioclient-audio_effect.md) structures.

Set the state of an audio effect by calling [IAudioEffectsManager::SetAudioEffectState](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md).

## -see-also

[IAudioEffectsManager::GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md)

[IAudioEffectsManager::SetAudioEffectState](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md)

[AUDIO_EFFECT](ns-audioclient-audio_effect.md)

