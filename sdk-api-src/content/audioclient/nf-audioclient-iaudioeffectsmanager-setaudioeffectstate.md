---
UID: NF:audioclient.IAudioEffectsManager.SetAudioEffectState
tech.root: CoreAudio
title: IAudioEffectsManager::SetAudioEffectState
description: The IAudioEffectsManager::SetAudioEffectState method (audioclient.h) sets the state of the specified audio effect.
ms.date: 08/16/2022
targetos: Windows
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
| AUDCLNT_E_EFFECT_NOT_AVAILABLE | The specified effect is not available |
| AUDCLNT_E_EFFECT_STATE_READ_ONLY | The specified effect has a state that is read-only |
| AUDCLNT_E_DEVICE_INVALIDATED | The associated audio stream has been destroyed. |

## -remarks

Get the current list of audio effects for the associated audio stream by calling [GetAudioEffects](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md).

## Examples

The following example demonstrates using the [IAudioEffectsManager.SetAudioEffectState](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md) to disable the **AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION** effect.

```cpp
HRESULT TryDisablePlatformDeepNoiseSuppression(_In_ IAudioClient *client)
{
    wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
    RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));
    wil::unique_cotaskmem_array_ptr<AudioEffect> effects;
    UINT32 numEffects;
    RETURN_IF_FAILED(audioEffectsManager->GetAudioEffects(&effects, &numEffects));

    for (UINT32 i = 0; i < numEffects; i++)
    {
        if (effects[i].id == AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION)
        {
            // Check if deep noise suppression can be set and if it is currently on
            if (effects[i].canSetState && effects[i].state == AUDIO_EFFECT_STATE_ON)
            {
                HRESULT hr = audioEffectsManager->SetAudioEffectState(effects[i].id, AUDIO_EFFECT_STATE_OFF);

                // If canSetState changed to false, or the effect was removed, SetAudioEffectState
                // can fail with one of the following error codes.
                if (hr != AUDCLNT_E_EFFECT_NOT_AVAILABLE && hr != AUDCLNT_E_EFFECT_STATE_READ_ONLY)
                {
                    return hr;
                }
            }

            return S_OK;
        }
    }

    return S_OK;
}
```

The following example demonstrates using the [IAudioEffectsManager.SetAudioEffectState](nf-audioclient-iaudioeffectsmanager-setaudioeffectstate.md) to enable the **AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION** effect.

```cpp
HRESULT TryEnablePlatformDeepNoiseSuppression(_In_ IAudioClient *client)
{
    wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
    RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));
    wil::unique_cotaskmem_array_ptr<AUDIO_EFFECT> effects;
    UINT32 numEffects;
    RETURN_IF_FAILED(audioEffectsManager->GetAudioEffects(&effects, &numEffects));

    for (UINT32 i = 0; i < numEffects; i++)
    {
        if (effects[i].id == AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION)
        {
            // Check if deep noise suppression can be set and if it is currently off
            if (effects[i].canSetState && effects[i].state == AUDIO_EFFECT_STATE_OFF)
            {
                HRESULT hr = audioEffectsManager->SetAudioEffectState(effects[i].id, AUDIO_EFFECT_STATE_ON);

                // If canSetState changed to false, or the effect was removed, SetAudioEffectState
                // can fail with one of the following error codes.
                if (hr != AUDCLNT_E_EFFECT_NOT_AVAILABLE && hr != AUDCLNT_E_EFFECT_STATE_READ_ONLY)
                {
                    return hr;
                }
            }

            return S_OK;
        }
        }

        return S_OK;
}
```


## -see-also

