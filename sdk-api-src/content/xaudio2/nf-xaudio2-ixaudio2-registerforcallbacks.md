---
UID: NF:xaudio2.IXAudio2.RegisterForCallbacks
title: IXAudio2::RegisterForCallbacks (xaudio2.h)
description: Adds an IXAudio2EngineCallback pointer to the XAudio2 engine callback list.
helpviewer_keywords: ["IXAudio2 interface [XAudio2 Audio Mixing APIs]","RegisterForCallbacks method","IXAudio2.RegisterForCallbacks","IXAudio2::RegisterForCallbacks","RegisterForCallbacks","RegisterForCallbacks method [XAudio2 Audio Mixing APIs]","RegisterForCallbacks method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","xaudio2.ixaudio2_interface_registerforcallbacks","xaudio2/IXAudio2::RegisterForCallbacks"]
old-location: xaudio2\ixaudio2_interface_registerforcallbacks.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.RegisterForCallbacks(IXAudio2EngineCallback)
ms.date: 12/05/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],RegisterForCallbacks method, IXAudio2.RegisterForCallbacks, IXAudio2::RegisterForCallbacks, RegisterForCallbacks, RegisterForCallbacks method [XAudio2 Audio Mixing APIs], RegisterForCallbacks method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_registerforcallbacks, xaudio2/IXAudio2::RegisterForCallbacks
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
 - IXAudio2::RegisterForCallbacks
 - xaudio2/IXAudio2::RegisterForCallbacks
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
 - IXAudio2.RegisterForCallbacks
---

# IXAudio2::RegisterForCallbacks


## -description

Adds an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer to the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">XAudio2</a> engine callback list.

## -parameters

### -param pCallback [in]

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer to add to the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">XAudio2</a> engine callback list.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

This method can be called multiple times, allowing different components or layers of the same application to manage their own engine callback implementations separately.



It is invalid to call <b>RegisterForCallbacks</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If <b>RegisterForCallbacks</b> is called within a callback, it returns XAUDIO2_E_INVALID_CALL.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>