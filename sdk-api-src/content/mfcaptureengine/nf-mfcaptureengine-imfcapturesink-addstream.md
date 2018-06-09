---
UID: NF:mfcaptureengine.IMFCaptureSink.AddStream
title: IMFCaptureSink::AddStream
author: windows-sdk-content
description: Connects a stream from the capture source to this capture sink.
old-location: mf\imfcapturesink_addstream.htm
old-project: medfound
ms.assetid: 5D7A1FE0-92B9-4CC4-A268-17FA848055A9
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: AddStream, AddStream method [Media Foundation], AddStream method [Media Foundation],IMFCaptureSink interface, IMFCaptureSink interface [Media Foundation],AddStream method, IMFCaptureSink.AddStream, IMFCaptureSink::AddStream, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesink_addstream, mfcaptureengine/IMFCaptureSink::AddStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSink.AddStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureSink::AddStream


## -description


Connects a stream from the capture source to this capture sink.


## -parameters




### -param dwSourceStreamIndex [in]

The source stream to connect. The value can be any of the following.

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
The zero-based index of a stream. To get the number of streams, call <a href="https://msdn.microsoft.com/0CD466EF-4753-42F6-A9B9-71CBB0668342">IMFCaptureSource::GetDeviceStreamCount</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM"></a><a id="mf_capture_engine_first_source_photo_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM</b></b></dt>
<dt>0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The first image stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM"></a><a id="mf_capture_engine_first_source_video_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM</b></b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM"></a><a id="mf_capture_engine_first_source_audio_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM</b></b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
</table>
 


### -param pMediaType [in]

An <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> pointer that specifies the desired format of the output stream. The details of the format will depend on the capture sink.

<ul>
<li>Photo sink: A still image format compatible with <a href="https://msdn.microsoft.com/b872baf9-9fcb-4604-a518-26e109eda792">Windows Imaging Component</a> (WIC).</li>
<li>Preview sink: An uncompressed audio or video format.</li>
<li>Record sink: The audio or video format that will be written to the output file.</li>
</ul>

### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. For compressed streams, you can use this parameter to configure the encoder. This parameter can also be <b>NULL</b>.

For the preview sink, set this parameter to <b>NULL</b>.


### -param pdwSinkStreamIndex [out]

Receives the index of the new stream on the capture sink. Note that this index will not necessarily match the value of <i>dwSourceStreamIndex</i>. 


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
The format specified in <i>pMediaType</i> is not valid for this capture sink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSourceStreamIndex</i> parameter is invalid, or the specified source stream was already connected to this sink.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>
 

 

