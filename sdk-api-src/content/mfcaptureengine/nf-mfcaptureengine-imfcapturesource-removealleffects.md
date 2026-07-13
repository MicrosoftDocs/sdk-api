---
UID: NF:mfcaptureengine.IMFCaptureSource.RemoveAllEffects
title: IMFCaptureSource::RemoveAllEffects (mfcaptureengine.h)
description: Removes all effects from a capture stream.
helpviewer_keywords: ["IMFCaptureSource interface [Media Foundation]","RemoveAllEffects method","IMFCaptureSource.RemoveAllEffects","IMFCaptureSource::RemoveAllEffects","MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM","RemoveAllEffects","RemoveAllEffects method [Media Foundation]","RemoveAllEffects method [Media Foundation]","IMFCaptureSource interface","mf.imfcapturesource_removealleffects","mfcaptureengine/IMFCaptureSource::RemoveAllEffects"]
old-location: mf\imfcapturesource_removealleffects.htm
tech.root: mf
ms.assetid: C01F7A61-3585-4E8B-B914-7DB1446D1BC1
ms.date: 12/05/2018
ms.keywords: IMFCaptureSource interface [Media Foundation],RemoveAllEffects method, IMFCaptureSource.RemoveAllEffects, IMFCaptureSource::RemoveAllEffects, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, RemoveAllEffects, RemoveAllEffects method [Media Foundation], RemoveAllEffects method [Media Foundation],IMFCaptureSource interface, mf.imfcapturesource_removealleffects, mfcaptureengine/IMFCaptureSource::RemoveAllEffects
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
 - IMFCaptureSource::RemoveAllEffects
 - mfcaptureengine/IMFCaptureSource::RemoveAllEffects
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
 - IMFCaptureSource.RemoveAllEffects
---

# IMFCaptureSource::RemoveAllEffects


## -description

Removes all effects from a capture stream.

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
The zero-based index of a stream. To get the number of streams, call <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-getdevicestreamcount">IMFCaptureSource::GetDeviceStreamCount</a>.

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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSourceStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>