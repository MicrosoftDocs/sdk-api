---
UID: NF:mfidl.MFCreateAudioRendererActivate
title: MFCreateAudioRendererActivate function (mfidl.h)
description: Creates an activation object for the Streaming Audio Renderer.
helpviewer_keywords: ["MFCreateAudioRendererActivate","MFCreateAudioRendererActivate function [Media Foundation]","bce55c34-d64a-4f3b-8d09-6c9363e4eb11","mf.mfcreateaudiorendereractivate","mfidl/MFCreateAudioRendererActivate"]
old-location: mf\mfcreateaudiorendereractivate.htm
tech.root: medfound
ms.assetid: bce55c34-d64a-4f3b-8d09-6c9363e4eb11
ms.date: 12/05/2018
ms.keywords: MFCreateAudioRendererActivate, MFCreateAudioRendererActivate function [Media Foundation], bce55c34-d64a-4f3b-8d09-6c9363e4eb11, mf.mfcreateaudiorendereractivate, mfidl/MFCreateAudioRendererActivate
f1_keywords:
- mfidl/MFCreateAudioRendererActivate
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mf.dll
api_name:
- MFCreateAudioRendererActivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateAudioRendererActivate function


## -description



Creates an activation object for the <a href="https://docs.microsoft.com/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>.




## -parameters




### -param ppActivate [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. Use this interface to create the audio renderer. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the audio renderer, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> on the retrieved <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer.

<div class="alert"><b>Note</b>  To avoid a memory leak, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject">IMFActivate::ShutdownObject</a> before releasing the final reference to the audio renderer or the audio renderer activate object.</div>
<div> </div>
To configure the audio renderer, set any of the following attributes on the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object before calling <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a>. (If you are using the Media Session, the Media Session automatically calls <b>ActivateObject</b> when you queue the topology.)

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-audio-renderer-attribute-endpoint-id-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID</a>
</td>
<td>The audio endpoint device identifier.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-audio-renderer-attribute-endpoint-role-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE</a>
</td>
<td>The audio endpoint role.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-audio-renderer-attribute-flags-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS</a>
</td>
<td>Miscellaneous configuration flags.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-audio-renderer-attribute-session-id-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID</a>
</td>
<td>The audio policy class.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-audio-renderer-attribute-stream-category">MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY</a>
</td>
<td>The audio stream category.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-low-latency">MF_LOW_LATENCY</a>
</td>
<td>Enables low-latency audio streaming.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
 

 

