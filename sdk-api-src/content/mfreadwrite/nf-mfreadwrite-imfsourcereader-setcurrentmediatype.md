---
UID: NF:mfreadwrite.IMFSourceReader.SetCurrentMediaType
title: IMFSourceReader::SetCurrentMediaType
author: windows-driver-content
description: Sets the media type for a stream.
old-location: mf\imfsourcereader_setcurrentmediatype.htm
old-project: medfound
ms.assetid: 54caec4d-1393-487b-94ee-78563b2b4645
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFSourceReader interface [Media Foundation],SetCurrentMediaType method, IMFSourceReader.SetCurrentMediaType, IMFSourceReader::SetCurrentMediaType, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, SetCurrentMediaType, SetCurrentMediaType method [Media Foundation], SetCurrentMediaType method [Media Foundation],IMFSourceReader interface, mf.imfsourcereader_setcurrentmediatype, mfreadwrite/IMFSourceReader::SetCurrentMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSourceReader.SetCurrentMediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceReader::SetCurrentMediaType


## -description


Sets the media type for a stream.

This media type defines that format that the <a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a> produces as output. It can differ from the native format provided by the media source. See Remarks for more information.


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
 


### -param pdwReserved [in, out]

Reserved. Set to <b>NULL</b>.


### -param pMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDMEDIATYPE</b></b></dt>
</dl>
</td>
<td width="60%">
At least one decoder was found for the native stream type, but the type specified by <i>pMediaType</i> was rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
One or more sample requests are still pending.

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
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_TOPO_CODEC_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
Could not find a decoder for the native stream type.

</td>
</tr>
</table>
 




## -remarks



For each stream, you can set the media type to any of the following:

<ul>
<li>One of the native types offered by the media source. To enumerate the native types, call <a href="https://msdn.microsoft.com/4b514f8d-082f-4e84-b512-d4a59706a6d8">IMFSourceReader::GetNativeMediaType</a>.</li>
<li>If the native media type is compressed, you can specify a corresponding uncompressed format. The Source Reader will search for a decoder that can decode from the native format to the specified uncompressed format.</li>
</ul>
Audio resampling support was added to the source reader with Windows 8.  In versions of Windows prior to  Windows 8, the source reader does not support audio resampling. If you need to resample the audio in versions of Windows earlier than Windows 8, you can use the <a href="https://msdn.microsoft.com/bee755c4-0585-40fb-aa4d-4e964f5144a3">Audio Resampler DSP</a>.

If you set the <a href="https://msdn.microsoft.com/b1ec1c0e-8042-4486-822f-eb106577c0b1">MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING</a> attribute to <b>TRUE</b> when you create the Source Reader, the Source Reader will convert YUV video to RGB-32. This conversion is not optimized for real-time video playback.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

