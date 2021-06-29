---
UID: NF:xaudio2.IXAudio2.Release
title: IXAudio2::Release (xaudio2.h)
description: Releases a reference to the XAudio2 object.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","Release method","IXAudio2.Release","IXAudio2::Release","Release","Release method [XAudio2 Audio Mixing APIs]","Release method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_release","xaudio2/IXAudio2::Release"]
old-location: xaudio2\ixaudio2_interface_release.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.Release
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],Release method, IXAudio2.Release, IXAudio2::Release, Release, Release method [XAudio2 Audio Mixing APIs], Release method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_release, xaudio2/IXAudio2::Release
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
 - IXAudio2::Release
 - xaudio2/IXAudio2::Release
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
 - IXAudio2.Release
---

# IXAudio2::Release


## -description

Releases a reference to the XAudio2 object.



## -returns

Always returns 0.

## -remarks

When the final <b>Release</b> is called on a given XAudio2 object, all voice objects that are associated with it are destroyed. Any pointers to these objects that are still held by the client become invalid immediately. Any calls that are made to them cause undefined behavior. The audio processing engine is also stopped. This is so that after <b>Release</b> is returned, the client can safely free any data that is referenced by the graph (for example, audio source buffers or callback handling objects).



<b>Release</b> is a synchronous call. While glitching should not occur (since it only briefly takes the processing lock), a title can avoid potential thread wait times by calling this method in an XAudio2 callback.



It is invalid to call <b>Release</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>
