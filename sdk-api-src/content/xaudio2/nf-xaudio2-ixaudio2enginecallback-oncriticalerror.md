---
UID: NF:xaudio2.IXAudio2EngineCallback.OnCriticalError
title: IXAudio2EngineCallback::OnCriticalError (xaudio2.h)
description: Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.
helpviewer_keywords: ["IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs]","OnCriticalError method","IXAudio2EngineCallback.OnCriticalError","IXAudio2EngineCallback::OnCriticalError","OnCriticalError","OnCriticalError method [XAudio2 Audio Mixing APIs]","OnCriticalError method [XAudio2 Audio Mixing APIs]","IXAudio2EngineCallback interface","xaudio2.ixaudio2enginecallback_oncriticalerror","xaudio2/IXAudio2EngineCallback::OnCriticalError"]
old-location: xaudio2\ixaudio2enginecallback_oncriticalerror.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2enginecallback.IXAudio2EngineCallback.OnCriticalError(HRESULT)
ms.date: 12/05/2018
ms.keywords: IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs],OnCriticalError method, IXAudio2EngineCallback.OnCriticalError, IXAudio2EngineCallback::OnCriticalError, OnCriticalError, OnCriticalError method [XAudio2 Audio Mixing APIs], OnCriticalError method [XAudio2 Audio Mixing APIs],IXAudio2EngineCallback interface, xaudio2.ixaudio2enginecallback_oncriticalerror, xaudio2/IXAudio2EngineCallback::OnCriticalError
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
 - IXAudio2EngineCallback::OnCriticalError
 - xaudio2/IXAudio2EngineCallback::OnCriticalError
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
 - IXAudio2EngineCallback.OnCriticalError
---

# IXAudio2EngineCallback::OnCriticalError


## -description

Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.

## -parameters

### -param Error

Error code returned by XAudio2.

## -remarks

If you provide the ID of a  specific device in the <i>szDeviceId</i> parameter to   <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice">IXAudio2::CreateMasteringVoice</a> or use the XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT flag, then a critical error will occur and <b>OnCriticalError</b> is raised if the underlying WASAPI rendering device becomes unavailable. This can occur when a headset or speaker is unplugged or when a USB audio device is removed, for example.   Once a critical error has occurred, audio processing stops and all further calls to XAudio2 fail. The only way to recover in this situation is to release the XAudio2 instance and create a new one.





If you specified NULL or  <i>szDeviceId</i> parameter to   <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice">IXAudio2::CreateMasteringVoice</a>, then the system uses a Virtual Audio Client to represent the audio endpoint. In this case, if the underlying WASAPI rendering device becomes unavailable, the system automatically selects a new audio rendering device for rendering, audio processing continues, and <b>OnCriticalError</b> is not raised.

On the mobile device family, a Virtual Audio Client is always used and <b>OnCriticalError</b> is never raised, regardless of the values you provide to    <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice">CreateMasteringVoice</a>.

For information about the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> interface methods, see the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> section.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>