---
UID: NF:xaudio2.IXAudio2SourceVoice.Start
title: IXAudio2SourceVoice::Start (xaudio2.h)
description: Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device.
helpviewer_keywords: ["IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","Start method","IXAudio2SourceVoice.Start","IXAudio2SourceVoice::Start","Start","Start method [XAudio2 Audio Mixing APIs]","Start method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","xaudio2.ixaudio2sourcevoice_interface_start","xaudio2/IXAudio2SourceVoice::Start"]
old-location: xaudio2\ixaudio2sourcevoice_interface_start.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.Start(UINT32,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],Start method, IXAudio2SourceVoice.Start, IXAudio2SourceVoice::Start, Start, Start method [XAudio2 Audio Mixing APIs], Start method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_start, xaudio2/IXAudio2SourceVoice::Start
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
 - IXAudio2SourceVoice::Start
 - xaudio2/IXAudio2SourceVoice::Start
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
 - IXAudio2SourceVoice.Start
---

# IXAudio2SourceVoice::Start


## -description

Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device.

## -parameters

### -param X2DEFAULT

TBD

### -param Flags [in]

Flags that control how the voice is started. Must be 0.

### -param OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

If the XAudio2 engine is stopped, the voice stops running. However, it remains in the started state, so that it starts running again as soon as the engine starts.



When first created, source voices are in the stopped state. Submix and mastering voices are in the started state.



After <b>Start</b> is called it has no further effect if called again before <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop">IXAudio2SourceVoice::Stop</a> is called. In addition multiple calls to <b>Start</b> without matching calls to <b>IXAudio2SourceVoice::Stop</b> will result in warning messages in debug builds.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>