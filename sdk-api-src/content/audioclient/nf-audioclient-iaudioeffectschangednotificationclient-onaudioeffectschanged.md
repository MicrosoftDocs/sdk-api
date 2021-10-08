---
UID: NF:audioclient.IAudioEffectsChangedNotificationClient.OnAudioEffectsChanged
tech.root: CoreAudio
title: IAudioEffectsChangedNotificationClient::OnAudioEffectsChanged
ms.date: 06/16/2021
targetos: Windows
description: Called by the system when the list of audio effects changes or the resources needed to enable an effect changes.
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
 - IAudioEffectsChangedNotificationClient::OnAudioEffectsChanged
f1_keywords:
 - IAudioEffectsChangedNotificationClient::OnAudioEffectsChanged
 - audioclient/IAudioEffectsChangedNotificationClient::OnAudioEffectsChanged
dev_langs:
 - c++
---

## -description

Called by the system when the list of audio effects changes or the resources needed to enable an effect changes, i.e. when the value of the *canSetState* field of the associated [AUDIO_EFFECT](ns-audioclient-audio_effect.md) changes.

## -returns

An HRESULT.

## -remarks

Register the callback interface by calling [IAudioEffectsManager::RegisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-registeraudioeffectschangednotificationcallback.md).

## -see-also

