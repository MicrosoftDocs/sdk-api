---
UID: NN:audioclient.IAudioClientDuckingControl
tech.root: CoreAudio
title: IAudioClientDuckingControl
ms.date: 02/08/2021
ms.topic: language-reference
targetos: Windows
description: Provides a method, SetDuckingOptionsForCurrentStream, that allows an app to specify that the system shouldn't duck the audio of other streams when the app's audio render stream is active.
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioclient.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
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
 - IAudioClientDuckingControl
f1_keywords:
 - IAudioClientDuckingControl
 - audioclient/IAudioClientDuckingControl
offlinehelp_keywords:
 - IAudioClientDuckingControl
 - audioclient/IAudioClientDuckingControl
dev_langs:
 - c++
---

## -description

Provides a method, [SetDuckingOptionsForCurrentStream](nf-audioclient-iaudioclientduckingcontrol-setduckingoptionsforcurrentstream.md), that allows an app to specify that the system shouldn't duck the audio of other streams when the app's audio render stream is active.


## -remarks

Get an instance of the **IAudioClientDuckingControl** interface by calling [IAudioClient::GetService](nf-audioclient-iaudioclient-getservice.md), passing in the interface ID constant **IID_IAudioClientDuckingControl**.

**IAudioClientDuckingControl** only controls the ducking caused by the audio stream (**IAudioClient**) that the interface is obtained from. 

Audio from applications could continue to be ducked if there are other concurrent applications with streams that cause ducking.

## -see-also

