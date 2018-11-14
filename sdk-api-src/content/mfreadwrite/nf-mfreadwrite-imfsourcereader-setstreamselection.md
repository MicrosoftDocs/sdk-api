---
UID: NF:mfreadwrite.IMFSourceReader.SetStreamSelection
title: IMFSourceReader::SetStreamSelection
author: windows-sdk-content
description: Selects or deselects one or more streams.
old-location: mf\imfsourcereader_setstreamselection.htm
tech.root: medfound
ms.assetid: 5efadce6-347c-48cf-b42c-d461922b2523
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSourceReader interface [Media Foundation],SetStreamSelection method, IMFSourceReader.SetStreamSelection, IMFSourceReader::SetStreamSelection, MF_SOURCE_READER_ALL_STREAMS, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFSourceReader interface, mf.imfsourcereader_setstreamselection, mfreadwrite/IMFSourceReader::SetStreamSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFSourceReader.SetStreamSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfreadwrite.h
: 
- IMFSourceReader.SetStreamSelection
: 
---

# IMFSourceReader::SetStreamSelection


## -description


Selects or deselects one or more streams.


## -parameters




### -param dwStreamIndex [in]

The stream to set. The value can be any of the following.

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
<tr>
<td width="40%"><a id="MF_SOURCE_READER_ALL_STREAMS"></a><a id="mf_source_reader_all_streams"></a><dl>
<dt><b><b>MF_SOURCE_READER_ALL_STREAMS</b></b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
All streams.

</td>
</tr>
</table>
 


### -param fSelected [in]

Specify <b>TRUE</b> to select streams or <b>FALSE</b> to deselect streams. If a stream is deselected, it will not generate data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There are two common uses for this method:

<ul>
<li>To change the default stream selection. Some media files contain multiple streams of the same type. For example, a file might include audio streams for multiple languages. You can use this method to change which of the streams is selected. To get information about each stream, call <a href="https://msdn.microsoft.com/40544e1e-cce2-4860-aeb2-b60696b09145">IMFSourceReader::GetPresentationAttribute</a>  or <a href="https://msdn.microsoft.com/4b514f8d-082f-4e84-b512-d4a59706a6d8">IMFSourceReader::GetNativeMediaType</a>.</li>
<li>If you will not need data from one of the streams, it is a good idea to deselect that stream. If the stream is selected, the media source might hold onto a queue of unread data, and the queue might grow indefinitely, consuming memory. </li>
</ul>
For an example of deselecting a stream, see <a href="tutorial__decoding_audio.htm">Tutorial: Decoding Audio</a>.

If a stream is deselected, the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method returns <b>MF_E_INVALIDREQUEST</b> for that stream. Other <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> methods are valid for deselected streams.

Stream selection does not affect how the source reader loads or unloads decoders in memory. In particular, deselecting a stream does not force the source reader to unload the decoder for that stream.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

