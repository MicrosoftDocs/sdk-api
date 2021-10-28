---
UID: NN:xaudio2.IXAudio2EngineCallback
title: IXAudio2EngineCallback (xaudio2.h)
description: The IXAudio2EngineCallback interface contains methods that notify the client when certain events happen in the IXAudio2 engine.
helpviewer_keywords: ["IXAudio2EngineCallback","IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs]","IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2enginecallback","xaudio2/IXAudio2EngineCallback"]
old-location: xaudio2\ixaudio2enginecallback.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2enginecallback.IXAudio2EngineCallback
ms.date: 12/05/2018
ms.keywords: IXAudio2EngineCallback, IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs], IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2enginecallback, xaudio2/IXAudio2EngineCallback
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
 - IXAudio2EngineCallback
 - xaudio2/IXAudio2EngineCallback
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
 - IXAudio2EngineCallback
---

# IXAudio2EngineCallback interface


## -description

The IXAudio2EngineCallback interface contains methods that notify the client when certain events happen in the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a> engine.

This interface should be implemented by the XAudio2 client. XAudio2 calls these methods via an interface pointer provided by the client, using the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create">XAudio2Create</a> method. Methods in this interface return <b>void</b>, rather than an HRESULT. 


See <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> for restrictions on callback implementation.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror">OnCriticalError</a>
</td>
<td align="left" width="63%">
Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend">OnProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just after an audio processing pass ends.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart">OnProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just before an audio processing pass begins.

</td>
</tr>
</table>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>



<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>
