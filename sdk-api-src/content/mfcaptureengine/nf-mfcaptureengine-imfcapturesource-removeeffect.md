---
UID: NF:mfcaptureengine.IMFCaptureSource.RemoveEffect
title: IMFCaptureSource::RemoveEffect (mfcaptureengine.h)
description: Removes an effect from a capture stream.
helpviewer_keywords: ["IMFCaptureSource interface [Media Foundation]","RemoveEffect method","IMFCaptureSource.RemoveEffect","IMFCaptureSource::RemoveEffect","MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM","RemoveEffect","RemoveEffect method [Media Foundation]","RemoveEffect method [Media Foundation]","IMFCaptureSource interface","mf.imfcapturesource_removeeffect","mfcaptureengine/IMFCaptureSource::RemoveEffect"]
old-location: mf\imfcapturesource_removeeffect.htm
tech.root: mf
ms.assetid: 5FF2EF1C-1BF0-4CF7-95AB-1BB10025D66F
ms.date: 12/05/2018
ms.keywords: IMFCaptureSource interface [Media Foundation],RemoveEffect method, IMFCaptureSource.RemoveEffect, IMFCaptureSource::RemoveEffect, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, RemoveEffect, RemoveEffect method [Media Foundation], RemoveEffect method [Media Foundation],IMFCaptureSource interface, mf.imfcapturesource_removeeffect, mfcaptureengine/IMFCaptureSource::RemoveEffect
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFCaptureSource::RemoveEffect
 - mfcaptureengine/IMFCaptureSource::RemoveEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSource.RemoveEffect
---

# IMFCaptureSource::RemoveEffect


## -description

Removes an effect from a capture stream.

## -parameters

### -param dwSourceStreamIndex [in]

The capture stream. The value can be any of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0–0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The zero-based index of a stream.  To get the number of streams, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getdevicestreamcount">IMFCaptureSource::GetDeviceStreamCount</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM"></a><a id="mf_capture_engine_first_source_photo_stream"></a><dl>
<dt><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM</b></dt>
<dt>0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The first image stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM"></a><a id="mf_capture_engine_first_source_video_stream"></a><dl>
<dt><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM</b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM"></a><a id="mf_capture_engine_first_source_audio_stream"></a><dl>
<dt><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM</b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
</table>

### -param pUnknown [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the effect object.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request. Possibly the specified effect could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSourceStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

This method removes an effect that was previously added using the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-addeffect">IMFCaptureSource::AddEffect</a> method.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>