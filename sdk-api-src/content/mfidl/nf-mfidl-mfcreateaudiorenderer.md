---
UID: NF:mfidl.MFCreateAudioRenderer
title: MFCreateAudioRenderer function (mfidl.h)
description: Creates the Streaming Audio Renderer.
helpviewer_keywords: ["9554e39b-9d14-4b7f-862c-a1ffcf84543c","MFCreateAudioRenderer","MFCreateAudioRenderer function [Media Foundation]","mf.mfcreateaudiorenderer","mfidl/MFCreateAudioRenderer"]
old-location: mf\mfcreateaudiorenderer.htm
tech.root: mf
ms.assetid: 9554e39b-9d14-4b7f-862c-a1ffcf84543c
ms.date: 12/05/2018
ms.keywords: 9554e39b-9d14-4b7f-862c-a1ffcf84543c, MFCreateAudioRenderer, MFCreateAudioRenderer function [Media Foundation], mf.mfcreateaudiorenderer, mfidl/MFCreateAudioRenderer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateAudioRenderer
 - mfidl/MFCreateAudioRenderer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateAudioRenderer
---

# MFCreateAudioRenderer function


## -description

Creates the <a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>.

## -parameters

### -param pAudioAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which is used to configure the audio renderer. This parameter can be <b>NULL</b>. See Remarks.

### -param ppSink [out]

Receives a pointer to the audio renderer's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To configure the audio renderer, set any of the following attributes on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface specified in the <i>pAudioAttributes</i> parameter.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-audio-renderer-attribute-endpoint-id-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID</a>
</td>
<td>The audio endpoint device identifier.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-audio-renderer-attribute-endpoint-role-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE</a>
</td>
<td>The audio endpoint role.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-audio-renderer-attribute-flags-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS</a>
</td>
<td>Miscellaneous configuration flags.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-audio-renderer-attribute-session-id-attribute">MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID</a>
</td>
<td>The audio policy class.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-audio-renderer-attribute-stream-category">MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY</a>
</td>
<td>The audio stream category.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-low-latency">MF_LOW_LATENCY</a>
</td>
<td>Enables low-latency audio streaming.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>