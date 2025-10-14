---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCurrentDeviceMediaType
title: IMFCaptureSource::GetCurrentDeviceMediaType (mfcaptureengine.h)
description: Gets the current media type for a capture stream.
helpviewer_keywords: ["GetCurrentDeviceMediaType","GetCurrentDeviceMediaType method [Media Foundation]","GetCurrentDeviceMediaType method [Media Foundation]","IMFCaptureSource interface","IMFCaptureSource interface [Media Foundation]","GetCurrentDeviceMediaType method","IMFCaptureSource.GetCurrentDeviceMediaType","IMFCaptureSource::GetCurrentDeviceMediaType","MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM","MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM","mf.imfcapturesource_getcurrentdevicemediatype","mfcaptureengine/IMFCaptureSource::GetCurrentDeviceMediaType"]
old-location: mf\imfcapturesource_getcurrentdevicemediatype.htm
tech.root: mf
ms.assetid: 8F263F5C-D1B4-4DF7-AFCB-E27575FBAAA2
ms.date: 12/05/2018
ms.keywords: GetCurrentDeviceMediaType, GetCurrentDeviceMediaType method [Media Foundation], GetCurrentDeviceMediaType method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetCurrentDeviceMediaType method, IMFCaptureSource.GetCurrentDeviceMediaType, IMFCaptureSource::GetCurrentDeviceMediaType, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesource_getcurrentdevicemediatype, mfcaptureengine/IMFCaptureSource::GetCurrentDeviceMediaType
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
 - IMFCaptureSource::GetCurrentDeviceMediaType
 - mfcaptureengine/IMFCaptureSource::GetCurrentDeviceMediaType
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
 - IMFCaptureSource.GetCurrentDeviceMediaType
---

# IMFCaptureSource::GetCurrentDeviceMediaType


## -description

Gets the current media type for a capture stream.

## -parameters

### -param dwSourceStreamIndex [in]

Specifies which stream to query. The value can be any of the following.

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

### -param ppMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

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