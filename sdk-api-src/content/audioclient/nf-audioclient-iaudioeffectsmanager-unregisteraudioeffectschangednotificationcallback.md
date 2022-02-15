---
UID: NF:audioclient.IAudioEffectsManager.UnregisterAudioEffectsChangedNotificationCallback
tech.root: CoreAudio
title: IAudioEffectsManager::UnregisterAudioEffectsChangedNotificationCallback
ms.date: 06/21/2021
targetos: Windows
description: Unregisters an IAudioEffectsChangedNotificationClient interface.
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
 - IAudioEffectsManager::UnregisterAudioEffectsChangedNotificationCallback
f1_keywords:
 - IAudioEffectsManager::UnregisterAudioEffectsChangedNotificationCallback
 - audioclient/IAudioEffectsManager::UnregisterAudioEffectsChangedNotificationCallback
dev_langs:
 - c++
---

## -description

Unregisters an [IAudioEffectsChangedNotificationClient](nn-audioclient-iaudioeffectschangednotificationclient.md) interface.

## -parameters

### -param client

The **IAudioEffectsChangedNotificationClient** interface to unregister.

## -returns

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| AUDCLNT_E_DEVICE_INVALIDATED | The associated audio stream has been destroyed. |

## -remarks

Register the callback interface by calling [RegisterAudioEffectsChangedNotificationCallback](nf-audioclient-iaudioeffectsmanager-registeraudioeffectschangednotificationcallback.md).


## -see-also

