---
UID: NF:spatialaudioclient.ISpatialAudioClient2.IsOffloadCapable
tech.root: CoreAudio
title: ISpatialAudioClient2::IsOffloadCapable
ms.date: 01/31/2022
targetos: Windows
description: Queries whether the audio rendering endpoint that the ISpatialAudioClient2 was created on supports hardware offloaded audio processing.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: spatialaudioclient.h
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient2::IsOffloadCapable
f1_keywords:
 - ISpatialAudioClient2::IsOffloadCapable
 - spatialaudioclient/ISpatialAudioClient2::IsOffloadCapable
dev_langs:
 - c++
---

## -description

Queries whether the audio rendering endpoint that the [ISpatialAudioClient2](nn-spatialaudioclient-ispatialaudioclient2) was created on supports hardware offloaded audio processing. The method also considers the capabilities of the [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) value that will be used, as use of offload is restricted to only certain **AUDIO_STREAM_CATEGORY** values.


## -parameters

### -param category [in]

A value from the [AUDIO_STREAM_CATEGORY](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration specifying the category of audio for which offload support is queried.

### -param isOffloadCapable [out]

Receives a boolean value indicating if offloaded audio processing is supported by the audio rendering endpoint.

## -returns

An HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK | Success |
| AUDCLNT_E_DEVICE_INVALIDATED | The audio device associated with the audio client has been invalidated. |
| E_INVALIDARG | The value supplied in the *category* parameter is not valid. |

## -remarks

## -see-also

