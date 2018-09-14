---
UID: NF:mfreadwrite.IMFSourceReaderEx.RemoveAllTransformsForStream
title: IMFSourceReaderEx::RemoveAllTransformsForStream
author: windows-sdk-content
description: Removes all of the Media Foundation transforms (MFTs) for a specified stream, with the exception of the decoder.
old-location: mf\imfsourcereaderex_removealltransformsforstream.htm
tech.root: medfound
ms.assetid: 6C0617CA-8F85-4854-9E4B-8F4300FAE8E3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFSourceReaderEx interface [Media Foundation],RemoveAllTransformsForStream method, IMFSourceReaderEx.RemoveAllTransformsForStream, IMFSourceReaderEx::RemoveAllTransformsForStream, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, RemoveAllTransformsForStream, RemoveAllTransformsForStream method [Media Foundation], RemoveAllTransformsForStream method [Media Foundation],IMFSourceReaderEx interface, mf.imfsourcereaderex_removealltransformsforstream, mfreadwrite/IMFSourceReaderEx::RemoveAllTransformsForStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderEx.RemoveAllTransformsForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderEx::RemoveAllTransformsForStream


## -description


Removes all of the Media Foundation transforms (MFTs) for a specified stream, with the exception of the decoder.


## -parameters




### -param dwStreamIndex [in]

The stream for which to remove the MFTs. The value can be any of the following.

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



Calling this method can reset the current output type for the stream. To get the new output type, call <a href="https://msdn.microsoft.com/c0fe3b34-42ad-45e4-812d-679bbe01a200">IMFSourceReader::GetCurrentMediaType</a>.

In asynchronous mode, this method fails if a sample request is pending. In that case, wait for the <a href="https://msdn.microsoft.com/1f334b49-d297-478d-a037-2fc53a75ed52">OnReadSample</a> callback to be invoked before calling the method. For more information about using the Source Reader in asynchronous mode, see <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a>.




## -see-also




<a href="https://msdn.microsoft.com/59888F9B-C464-4045-AA77-03EE16E2B598">IMFSourceReaderEx</a>
 

 

