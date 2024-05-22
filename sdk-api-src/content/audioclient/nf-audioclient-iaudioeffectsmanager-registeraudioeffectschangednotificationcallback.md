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


## Examples

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

[UnregisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-unregisteraudioeffectschangednotificationcallback.md)

