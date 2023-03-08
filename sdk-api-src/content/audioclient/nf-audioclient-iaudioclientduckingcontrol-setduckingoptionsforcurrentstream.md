---
UID: NF:audioclient.IAudioClientDuckingControl.SetDuckingOptionsForCurrentStream
tech.root: CoreAudio
title: IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
ms.date: 02/08/2021
ms.topic: language-reference
targetos: Windows
description: Sets the audio ducking options for an audio render stream.
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
req.target-min-winverclnt: Windows 10 Build 20348
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
 - IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
f1_keywords:
 - IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
 - audioclient/IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
helpviewer_keywords:
 - IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
 - audioclient/IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
dev_langs:
 - c++
---

## -description

Sets the audio ducking options for an audio render stream. Allows an app to specify that the system shouldn't duck the audio of other streams when the app's audio render stream is active.

## -parameters

### -param options

A value from the [AUDIO_DUCKING_OPTIONS](ne-audioclient-audio_ducking_options.md) enumeration specifying the requested ducking behavior.

## -returns

On successful completion, returns S_OK.

## -remarks

Get an instance of the [IAudioClientDuckingControl](nn-audioclient-iaudioclientduckingcontrol.md) interface by calling [IAudioClient::GetService](nf-audioclient-iaudioclient-getservice.md), passing in the interface ID constant **IID_IAudioClientDuckingControl**.

**IAudioClientDuckingControl** only controls the ducking caused by the audio stream (**IAudioClient**) that the interface is obtained from. 

Audio from applications could continue to be ducked if there are other concurrent applications with streams that cause ducking.


## -see-also

