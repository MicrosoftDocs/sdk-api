---
UID: NS:audioclient.AudioClientProperties~r1
title: AudioClientProperties
description: The AudioClientProperties structure (audioclient.h) is used to set the parameters that describe the properties of the client's audio stream.
ms.date: 08/16/2022
ms.keywords: AudioClientProperties
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioclient.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: AudioClientProperties
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - AudioClientProperties
 - audioclient/AudioClientProperties
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclient.h
api_name:
 - AudioClientProperties
---

# AudioClientProperties structure


## -description

The <b>AudioClientProperties</b> structure is used to set the parameters that describe the properties of the client's audio stream.

## -struct-fields

### -field cbSize

The size of the <b>AudioClientProperties</b> structure, in bytes.

### -field bIsOffload

Boolean value to indicate whether or not the audio stream is hardware-offloaded.

### -field eCategory

An enumeration that is used to specify the category of the audio stream.


### - Options

A member of the <a href="/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions">AUDCLNT_STREAMOPTIONS</a> enumeration describing the characteristics of the stream.

Supported in Windows 8.1 and later.

## -remarks

Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">IAudioClient2::SetClientProperties</a> and set the <i>bIsOffload</i> parameter of the <b>AudioClientProperties</b> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions">AUDCLNT_STREAMOPTIONS</a>



<a href="/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category">AUDIO_STREAM_CATEGORY</a>



<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">IAudioClient2::SetClientProperties</a>