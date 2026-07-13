---
UID: NF:mfreadwrite.IMFSourceReaderEx.AddTransformForStream
title: IMFSourceReaderEx::AddTransformForStream (mfreadwrite.h)
description: Adds a transform, such as an audio or video effect, to a stream.
helpviewer_keywords: ["AddTransformForStream","AddTransformForStream method [Media Foundation]","AddTransformForStream method [Media Foundation]","IMFSourceReaderEx interface","IMFSourceReaderEx interface [Media Foundation]","AddTransformForStream method","IMFSourceReaderEx.AddTransformForStream","IMFSourceReaderEx::AddTransformForStream","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","mf.imfsourcereaderex_addtransformforstream","mfreadwrite/IMFSourceReaderEx::AddTransformForStream"]
old-location: mf\imfsourcereaderex_addtransformforstream.htm
tech.root: mf
ms.assetid: 493BB3CF-044D-4E83-9FF7-BD2039358501
ms.date: 12/05/2018
ms.keywords: AddTransformForStream, AddTransformForStream method [Media Foundation], AddTransformForStream method [Media Foundation],IMFSourceReaderEx interface, IMFSourceReaderEx interface [Media Foundation],AddTransformForStream method, IMFSourceReaderEx.AddTransformForStream, IMFSourceReaderEx::AddTransformForStream, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereaderex_addtransformforstream, mfreadwrite/IMFSourceReaderEx::AddTransformForStream
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFSourceReaderEx::AddTransformForStream
 - mfreadwrite/IMFSourceReaderEx::AddTransformForStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderEx.AddTransformForStream
---

# IMFSourceReaderEx::AddTransformForStream


## -description

Adds a transform, such as an audio or video effect, to a stream.

## -parameters

### -param dwStreamIndex [in]

The stream to configure. The value can be any of the following.

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
The zero-based index of a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_VIDEO_STREAM"></a><a id="mf_source_reader_first_video_stream"></a><dl>
<dt><b>MF_SOURCE_READER_FIRST_VIDEO_STREAM</b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_AUDIO_STREAM"></a><a id="mf_source_reader_first_audio_stream"></a><dl>
<dt><b>MF_SOURCE_READER_FIRST_AUDIO_STREAM</b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
</table>

### -param pTransformOrActivate [in]

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
The transform does not support the current stream format, and no conversion was possible. See Remarks for more information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

This method attempts to add the transform at the end of the current processing chain. 

To use this method, make the following sequence of calls:

<ol>
<li>Call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">IMFSourceReader::SetCurrentMediaType</a> to set the output type that you want for the stream. In this step, you can specify a media type that contains only the major type and subtype GUIDs. For example, to get 32-bit RGB output, set a major type of <b>MFMediaType_Video</b> and a subtype of <b>MFVideoFormat_RGB32</b>. (For more information, see <a href="/windows/desktop/medfound/media-type-guids">Media Type GUIDs</a>.)</li>
<li>Call <b>AddTransformForStream</b>. If the Source Reader successfully connects the transform, it sets the output type on the transform.</li>
<li>Call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype">IMFSourceReader::GetCurrentMediaType</a> to get the output type from the transform. This method returns a media type with a complete format description.</li>
<li>Optionally, if you want to modify the output type, call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">IMFSourceReader::SetCurrentMediaType</a> again to set a complete media type on the transform.</li>
</ol>
The <b>AddTransformForStream</b> method will not insert a decoder into the processing chain. If the native stream format is encoded, and the transform requires an uncompressed format, call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">SetCurrentMediaType</a> to set the uncompressed format (step 1 in the previous list). However, the method will insert a video processor to convert between RGB and YUV formats, if required.

The method fails if the source reader was configured with the <a href="/windows/desktop/medfound/mf-readwrite-disable-converters">MF_READWRITE_DISABLE_CONVERTERS</a> or <a href="/windows/desktop/medfound/mf-source-reader-enable-video-processing">MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING</a> attributes. 

In asynchronous mode, the method also fails if a sample request is pending. In that case, wait for the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample">OnReadSample</a> callback to be invoked before calling the method. For more information about using the Source Reader in asynchronous mode, see <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a>.

You can add a transform at any time during streaming. However, the method does not flush or drain the pipeline before inserting the transform. Therefore, if data is already in the pipeline, the next sample is not guaranteed to have the transform applied.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex">IMFSourceReaderEx</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>