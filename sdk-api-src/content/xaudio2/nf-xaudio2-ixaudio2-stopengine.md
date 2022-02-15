---
UID: NF:xaudio2.IXAudio2.StopEngine
title: IXAudio2::StopEngine (xaudio2.h)
description: Stops the audio processing thread.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","StopEngine method","IXAudio2.StopEngine","IXAudio2::StopEngine","StopEngine","StopEngine method [XAudio2 Audio Mixing APIs]","StopEngine method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_stopengine","xaudio2/IXAudio2::StopEngine"]
old-location: xaudio2\ixaudio2_interface_stopengine.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.StopEngine
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],StopEngine method, IXAudio2.StopEngine, IXAudio2::StopEngine, StopEngine, StopEngine method [XAudio2 Audio Mixing APIs], StopEngine method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_stopengine, xaudio2/IXAudio2::StopEngine
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
 - IXAudio2::StopEngine
 - xaudio2/IXAudio2::StopEngine
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
 - IXAudio2.StopEngine
---

# IXAudio2::StopEngine


## -description

Stops the audio processing thread.



## -remarks

When <b>StopEngine</b> is called, all output is stopped immediately. However, the audio graph is left untouched, preserving effect parameters, effect histories (for example, the data stored by a reverb effect in order to emit echoes of a previous sound), voice states, pending source buffers, cursor positions, and so forth. When the engine is restarted, the resulting audio output will be identical—apart from a period of silence—to the output that would have been produced if the engine had never been stopped.



It is invalid to call <b>StopEngine</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>
