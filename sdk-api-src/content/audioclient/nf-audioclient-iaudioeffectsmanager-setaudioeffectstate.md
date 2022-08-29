---
UID: NF:audioclient.IAudioEffectsManager.SetAudioEffectState
tech.root: 
title: IAudioEffectsManager::SetAudioEffectState
description: The IAudioEffectsManager::SetAudioEffectState method (audioclient.h) sets the state of the specified audio effect.
ms.date: 08/16/2022
targetos: Windows
description: 
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
 - IAudioEffectsManager::SetAudioEffectState
f1_keywords:
 - IAudioEffectsManager::SetAudioEffectState
 - audioclient/IAudioEffectsManager::SetAudioEffectState
dev_langs:
 - c++
---

## -description

Sets the state of the specified audio effect.

## -parameters

### -param effectId

The GUID identifier of the effect for which the state is being changed. Audio effect GUIDs are defined in [ksmedia.h](/windows-hardware/drivers/audio/ksmedia-h).

### -param state

A value from the [AUDIO_EFFECT_STATE](ne-audioclient-audio_effect_state.md) enumerating specifying the state to set.

## -returns

Returns an HRESULT including but not limited to the following.

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| AUDCLNT_E_EFFECT_NOT_AVAILABLE | The specifed effect is not available |
| AUDCLNT_E_EFFECT_STATE_READ_ONLY | The specified effect has a state that is read-only |
| AUDCLNT_E_DEVICE_INVALIDATED | The associated audio stream has been destroyed. |

## -remarks

Get the current list of audio effects for the associated audio stream by calling [GetAudioEffects](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md).

## -see-also

