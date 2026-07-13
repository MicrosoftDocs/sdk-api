---
UID: NN:xaudio2.IXAudio2SourceVoice
title: IXAudio2SourceVoice (xaudio2.h)
description: Use a source voice to submit audio data to the XAudio2 processing pipeline.
helpviewer_keywords: ["IXAudio2SourceVoice","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2sourcevoice","xaudio2/IXAudio2SourceVoice"]
old-location: xaudio2\ixaudio2sourcevoice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs], IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2sourcevoice, xaudio2/IXAudio2SourceVoice
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2SourceVoice
 - xaudio2/IXAudio2SourceVoice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2SourceVoice
---

# IXAudio2SourceVoice interface


## -description

Use a source voice to submit audio data to the XAudio2 processing pipeline.You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.

## -inheritance

The <b>IXAudio2SourceVoice</b> interface inherits from <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>. <b>IXAudio2SourceVoice</b> also has these types of members:

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--change-voice-pitch">How to: Change Voice Pitch</a>



<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>
