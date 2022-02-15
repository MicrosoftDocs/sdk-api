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

## -see-also

