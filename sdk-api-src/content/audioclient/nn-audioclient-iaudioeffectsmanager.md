---
UID: NN:audioclient.IAudioEffectsManager
tech.root: CoreAudio
title: IAudioEffectsManager
ms.date: 06/15/2021
targetos: Windows
description: Provides management functionality for the audio effects pipeline
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
 - IAudioEffectsManager
f1_keywords:
 - IAudioEffectsManager
 - audioclient/IAudioEffectsManager
dev_langs:
 - c++
---

## -description

Provides management functionality for the audio effects pipeline for the associated audio stream, allowing applications to get the current list of effects, set the state of effects, and to register for notifications when the list of effects or effect states change.

## -remarks

Get an instance of this interface by calling [IAudioClient::GetService](nf-audioclient-iaudioclient-getservice.md) passing in the interface pointer of the **IAudioEffectsManager** interface.

```cpp
wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));
```

## Examples

The following example demonstrates the [IAudioEffectsManager.GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md) to detect whether the [AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION](/windows-hardware/drivers/audio/audio-signal-processing-modes#clsids-for-system-effects) effect is present on the specified audio stream.

```cpp
HRESULT IsPlatformDeepNoiseSuppressionPresent(_In_ IAudioClient *client, _Out_ bool *isPresent)
{
    *isPresent = false;
    wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
    RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));
    wil::unique_cotaskmem_array_ptr<AUDIO_EFFECT> effects;
    UINT32 numEffects;
    RETURN_IF_FAILED(audioEffectsManager->GetAudioEffects(&effects, &numEffects));

    for (UINT32 i = 0; i < numEffects; i++)
    {
        // Check if noise suppression is part of the current effects
        if (effects[i].id == AUDIO_EFFECT_TYPE_DEEP_NOISE_SUPPRESSION)
        {
            *isPresent = true;
            return S_OK;
        }
    }

    return S_OK;
}
```

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

The following code example demonstrates a class that implements [IAudioEffectsChangedNotificationClient](nn-audioclient-iaudioeffectschangednotificationclient.md) to receive notifications when the list of audio effects changes or the resources needed to enable an effect changes. In the [OnAudioStreamEffectsChanged](nf-audioclient-iaudioeffectschangednotificationclient-onaudioeffectschanged.md) callback, the example calls [GetAudioEffects](nf-audioclient-iaudioeffectsmanager-getaudioeffects.md) to get the current list of effects.

```cpp
class AudioEffectsChangedHandler :
    public winrt::implements<AudioEffectsChangedHandler, IAudioEffectsChangedNotificationClient>
{

    public:
    AudioEffectsChangedHandler(_In_ IAudioClient *client) : m_client(client){}
    STDMETHOD(OnAudioEffectsChanged)()
    {
        OnAudioStreamEffectsChanged(m_client.get());
        return S_OK;
    }
    private:
    wil::com_ptr_nothrow<IAudioClient> m_client;

};

wil::com_ptr_nothrow<IAudioEffectsChangedNotificationClient> g_effectsChangedHandler;

HRESULT RegisterAudioStreamEffectsChangedEvent(_In_ IAudioClient *client)
{
    if (!g_effectsChangedHandler)
    {
        wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
        RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));

        // Register for the audio effects changed notification
        g_effectsChangedHandler = winrt::make<AudioEffectsChangedHandler>(client).get();
        RETURN_IF_NULL_ALLOC(g_effectsChangedHandler);

        return audioEffectsManager->RegisterAudioEffectsChangedNotificationCallback(
            g_effectsChangedHandler.get());
    }
    return S_OK;
}

HRESULT UnregisterAudioStreamEffectsChangedEvent(_In_ IAudioClient *client)
{
    if (g_effectsChangedHandler != nullptr)
    {
        wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
        RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));

        // Unregister from the audio effects changed notification 
        return audioEffectsManager->UnregisterAudioEffectsChangedNotificationCallback(
            g_effectsChangedHandler.get());
        }

        return S_OK;
}

HRESULT OnAudioStreamEffectsChanged(_In_ IAudioClient *client)
{
    // Re-query the list of effects since there was some change
    wil::com_ptr_nothrow<IAudioEffectsManager> audioEffectsManager;
    RETURN_IF_FAILED(client->GetService(IID_PPV_ARGS(&audioEffectsManager)));
    wil::unique_cotaskmem_array_ptr<AUDIO_EFFECT> effects;
    UINT32 numEffects;
    RETURN_IF_FAILED(audioEffectsManager->GetAudioEffects(&effects, &numEffects));

    for (UINT32 i = 0; i < numEffects; i++)
    {

        // Here the app can check which effects are still enabled, and check if there are new
        // effects that now can be enabled.
        // As an example, the following code enables any effect that can be enabled, if it is not
        // already enabled.
        if (effects[i].canSetState && effects[i].state == AUDIO_EFFECT_STATE_OFF)
        {
            HRESULT hr = audioEffectsManager->SetAudioEffectState(effects[i].id, AUDIO_EFFECT_STATE_ON));
            if (hr == AUDCLNT_E_EFFECT_NOT_AVAILABLE || hr == AUDCLNT_E_EFFECT_STATE_READ_ONLY)
            {
                hr = S_OK;
            }
            RETURN_IF_FAILED(hr);

        }
    }

    return S_OK;
}
```

## -see-also

