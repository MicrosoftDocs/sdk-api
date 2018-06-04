---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<dt><b><b>MF_SOURCE_READER_FIRST_VIDEO_STREAM</b></b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_AUDIO_STREAM"></a><a id="mf_source_reader_first_audio_stream"></a><dl>
<dt><b><b>MF_SOURCE_READER_FIRST_AUDIO_STREAM</b></b></dt>
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
<li>A Media Foundation transform (MFT) that exposes the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface.</li>
<li>An MFT activation object that exposes the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface.</li>
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
<dt><b><b>MF_E_INVALIDSTREAMNUMBER</b></b></dt>
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
<li>Call <a href="https://msdn.microsoft.com/54caec4d-1393-487b-94ee-78563b2b4645">IMFSourceReader::SetCurrentMediaType</a> to set the output type that you want for the stream. In this step, you can specify a media type that contains only the major type and subtype GUIDs. For example, to get 32-bit RGB output, set a major type of <b>MFMediaType_Video</b> and a subtype of <b>MFVideoFormat_RGB32</b>. (For more information, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Media Type GUIDs</a>.)</li>
<li>Call <b>AddTransformForStream</b>. If the Source Reader successfully connects the transform, it sets the output type on the transform.</li>
<li>Call <a href="https://msdn.microsoft.com/c0fe3b34-42ad-45e4-812d-679bbe01a200">IMFSourceReader::GetCurrentMediaType</a> to get the output type from the transform. This method returns a media type with a complete format description.</li>
<li>Optionally, if you want to modify the output type, call <a href="https://msdn.microsoft.com/54caec4d-1393-487b-94ee-78563b2b4645">IMFSourceReader::SetCurrentMediaType</a> again to set a complete media type on the transform.</li>
</ol>
The <b>AddTransformForStream</b> method will not insert a decoder into the processing chain. If the native stream format is encoded, and the transform requires an uncompressed format, call <a href="https://msdn.microsoft.com/54caec4d-1393-487b-94ee-78563b2b4645">SetCurrentMediaType</a> to set the uncompressed format (step 1 in the previous list). However, the method will insert a video processor to convert between RGB and YUV formats, if required.

The method fails if the source reader was configured with the <a href="https://msdn.microsoft.com/282b70c3-c81c-47dd-bfa2-7e77138ccb91">MF_READWRITE_DISABLE_CONVERTERS</a> or <a href="https://msdn.microsoft.com/b1ec1c0e-8042-4486-822f-eb106577c0b1">MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING</a> attributes. 

In asynchronous mode, the method also fails if a sample request is pending. In that case, wait for the <a href="https://msdn.microsoft.com/1f334b49-d297-478d-a037-2fc53a75ed52">OnReadSample</a> callback to be invoked before calling the method. For more information about using the Source Reader in asynchronous mode, see <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a>.

You can add a transform at any time during streaming. However, the method does not flush or drain the pipeline before inserting the transform. Therefore, if data is already in the pipeline, the next sample is not guaranteed to have the transform applied.




## -see-also




<a href="https://msdn.microsoft.com/59888F9B-C464-4045-AA77-03EE16E2B598">IMFSourceReaderEx</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

