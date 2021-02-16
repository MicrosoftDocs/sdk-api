---
UID: NF:xaudio2.IXAudio2.UnregisterForCallbacks
title: IXAudio2::UnregisterForCallbacks (xaudio2.h)
description: Removes an IXAudio2EngineCallback pointer from the XAudio2 engine callback list.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","UnregisterForCallbacks method","IXAudio2.UnregisterForCallbacks","IXAudio2::UnregisterForCallbacks","UnregisterForCallbacks","UnregisterForCallbacks method [XAudio2 Audio Mixing APIs]","UnregisterForCallbacks method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_unregisterforcallbacks","xaudio2/IXAudio2::UnregisterForCallbacks"]
old-location: xaudio2\ixaudio2_interface_unregisterforcallbacks.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.UnregisterForCallbacks(IXAudio2EngineCallback)
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],UnregisterForCallbacks method, IXAudio2.UnregisterForCallbacks, IXAudio2::UnregisterForCallbacks, UnregisterForCallbacks, UnregisterForCallbacks method [XAudio2 Audio Mixing APIs], UnregisterForCallbacks method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_unregisterforcallbacks, xaudio2/IXAudio2::UnregisterForCallbacks
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
 - IXAudio2::UnregisterForCallbacks
 - xaudio2/IXAudio2::UnregisterForCallbacks
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
 - IXAudio2.UnregisterForCallbacks
---

# IXAudio2::UnregisterForCallbacks


## -description

Removes an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer from the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">XAudio2</a> engine callback list.

## -parameters

### -param pCallback [in]

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer to remove from the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">XAudio2</a> engine callback list. 
If the given pointer is present more than once in the list, only the first instance in the list will be removed.

## -remarks

It is invalid to call <b>UnregisterForCallbacks</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>