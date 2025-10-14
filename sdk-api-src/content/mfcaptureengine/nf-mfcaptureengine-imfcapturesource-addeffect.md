---
UID: NF:mfcaptureengine.IMFCaptureSource.AddEffect
title: IMFCaptureSource::AddEffect (mfcaptureengine.h)
description: Adds an effect to a capture stream.
helpviewer_keywords: ["AddEffect","AddEffect method [Media Foundation]","AddEffect method [Media Foundation]","IMFCaptureSource interface","IMFCaptureSource interface [Media Foundation]","AddEffect method","IMFCaptureSource.AddEffect","IMFCaptureSource::AddEffect","MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM","mf.imfcapturesource_addeffect","mfcaptureengine/IMFCaptureSource::AddEffect"]
old-location: mf\imfcapturesource_addeffect.htm
tech.root: mf
ms.assetid: C108360D-0B8C-4539-9D78-A5559100086E
ms.date: 12/05/2018
ms.keywords: AddEffect, AddEffect method [Media Foundation], AddEffect method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],AddEffect method, IMFCaptureSource.AddEffect, IMFCaptureSource::AddEffect, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesource_addeffect, mfcaptureengine/IMFCaptureSource::AddEffect
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
 - IMFCaptureSource::AddEffect
 - mfcaptureengine/IMFCaptureSource::AddEffect
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
 - IMFCaptureSource.AddEffect
---

# IMFCaptureSource::AddEffect


## -description

Adds an effect to a capture stream.

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

A pointer to one of the following:



<ul>
<li>A Media Foundation transform (MFT) that exposes the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.</li>
<li>An MFT activation object that exposes the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface.</li>
</ul>

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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
No compatible media type could be found.

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

The effect must be implemented as a <a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transform</a> (MFT). The <i>pUnknown</i> parameter can point to an instance of the MFT, or to an activation object for the MFT. For more information, see <a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>.

The effect is applied to the stream before the data reaches the capture sinks.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a>