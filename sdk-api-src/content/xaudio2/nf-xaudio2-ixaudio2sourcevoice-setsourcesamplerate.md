---
UID: NF:xaudio2.IXAudio2SourceVoice.SetSourceSampleRate
title: IXAudio2SourceVoice::SetSourceSampleRate (xaudio2.h)
description: Reconfigures the voice to consume source data at a different sample rate than the rate specified when the voice was created.
helpviewer_keywords: ["IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","SetSourceSampleRate method","IXAudio2SourceVoice.SetSourceSampleRate","IXAudio2SourceVoice::SetSourceSampleRate","SetSourceSampleRate","SetSourceSampleRate method [XAudio2 Audio Mixing APIs]","SetSourceSampleRate method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","xaudio2.ixaudio2sourcevoice_interface_setsourcesamplerate","xaudio2/IXAudio2SourceVoice::SetSourceSampleRate"]
old-location: xaudio2\ixaudio2sourcevoice_interface_setsourcesamplerate.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.SetSourceSampleRate(UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],SetSourceSampleRate method, IXAudio2SourceVoice.SetSourceSampleRate, IXAudio2SourceVoice::SetSourceSampleRate, SetSourceSampleRate, SetSourceSampleRate method [XAudio2 Audio Mixing APIs], SetSourceSampleRate method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_setsourcesamplerate, xaudio2/IXAudio2SourceVoice::SetSourceSampleRate
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2SourceVoice::SetSourceSampleRate
 - xaudio2/IXAudio2SourceVoice::SetSourceSampleRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.SetSourceSampleRate
---

# IXAudio2SourceVoice::SetSourceSampleRate


## -description

Reconfigures the voice to consume source data at a different sample rate than the rate specified when the voice was created.

## -parameters

### -param NewSourceSampleRate [in]

The new sample rate the voice should process submitted data at. Valid sample rates are 1kHz to 200kHz.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of error codes.

## -remarks

The <b>SetSourceSampleRate</b> method supports reuse of XAudio2 voices by allowing a voice to play sounds with a variety of sample rates. To use <b>SetSourceSampleRate</b> the voice must have been created without the XAUDIO2_VOICE_NOPITCH or XAUDIO2_VOICE_NOSRC flags and must not have any buffers currently queued.



The typical use of <b>SetSourceSampleRate</b> is to support voice pooling. For example to support voice pooling an application would precreate all the voices it expects to use. Whenever a new sound will be played the application chooses an inactive voice or ,if all voices are busy, picks the least important voice and calls <b>SetSourceSampleRate</b> on the voice with the new sound's sample rate. After <b>SetSourceSampleRate</b> has been called on the voice, the application can immediately start submitting and playing buffers with the new sample rate. This allows the application to avoid the overhead of creating and destroying voices frequently during gameplay.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>