---
UID: NS:audioclient.AUDIO_EFFECT
tech.root: CoreAudio
title: AUDIO_EFFECT
ms.date: 06/16/2021
targetos: Windows
description: Represents an audio effect.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioclient.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_EFFECT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclient.h
api_name:
 - AUDIO_EFFECT
f1_keywords:
 - AUDIO_EFFECT
 - audioclient/AUDIO_EFFECT
dev_langs:
 - c++
---

## -description

Represents an audio effect.

## -struct-fields

### -field id

The GUID identifier for an audio effect. Audio effect GUIDs are defined in [ksmedia.h](/windows-hardware/drivers/audio/ksmedia-h).

### -field canSetState

A boolean value specifying whether the effect state can be modified.

### -field state

A member of the [AUDIO_EFFECT_STATE](ne-audioclient-audio_effect_state.md) enumeration specifying the state of the audio effect.

## -remarks

Get a list of **AUDIO_EFFECT** structures by calling [IAudioEffectsManager::GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md).

## -see-also

[IAudioEffectsManager::GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md)

