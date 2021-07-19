---
UID: NF:xaudio2.IXAudio2.StartEngine
title: IXAudio2::StartEngine (xaudio2.h)
description: Starts the audio processing thread.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","StartEngine method","IXAudio2.StartEngine","IXAudio2::StartEngine","StartEngine","StartEngine method [XAudio2 Audio Mixing APIs]","StartEngine method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_startengine","xaudio2/IXAudio2::StartEngine"]
old-location: xaudio2\ixaudio2_interface_startengine.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.StartEngine
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],StartEngine method, IXAudio2.StartEngine, IXAudio2::StartEngine, StartEngine, StartEngine method [XAudio2 Audio Mixing APIs], StartEngine method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_startengine, xaudio2/IXAudio2::StartEngine
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
 - IXAudio2::StartEngine
 - xaudio2/IXAudio2::StartEngine
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
 - IXAudio2.StartEngine
---

# IXAudio2::StartEngine


## -description

Starts the audio processing thread.



## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

After <b>StartEngine</b> is called, all started voices begin to consume audio. All enabled effects start running, and the resulting audio is sent to any connected output devices. When XAudio2 is first initialized, the engine is already in the started state.



It is invalid to call <b>StartEngine</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If <b>StartEngine</b> is called within a callback, it returns XAUDIO2_E_INVALID_CALL.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>
