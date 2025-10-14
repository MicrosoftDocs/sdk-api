---
UID: NF:mfreadwrite.IMFSourceReader.SetStreamSelection
title: IMFSourceReader::SetStreamSelection (mfreadwrite.h)
description: Selects or deselects one or more streams.
helpviewer_keywords: ["IMFSourceReader interface [Media Foundation]","SetStreamSelection method","IMFSourceReader.SetStreamSelection","IMFSourceReader::SetStreamSelection","MF_SOURCE_READER_ALL_STREAMS","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","SetStreamSelection","SetStreamSelection method [Media Foundation]","SetStreamSelection method [Media Foundation]","IMFSourceReader interface","mf.imfsourcereader_setstreamselection","mfreadwrite/IMFSourceReader::SetStreamSelection"]
old-location: mf\imfsourcereader_setstreamselection.htm
tech.root: mf
ms.assetid: 5efadce6-347c-48cf-b42c-d461922b2523
ms.date: 12/05/2018
ms.keywords: IMFSourceReader interface [Media Foundation],SetStreamSelection method, IMFSourceReader.SetStreamSelection, IMFSourceReader::SetStreamSelection, MF_SOURCE_READER_ALL_STREAMS, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFSourceReader interface, mf.imfsourcereader_setstreamselection, mfreadwrite/IMFSourceReader::SetStreamSelection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceReader::SetStreamSelection
 - mfreadwrite/IMFSourceReader::SetStreamSelection
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
 - IMFSourceReader.SetStreamSelection
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
<tr>
<td width="40%"><a id="MF_SOURCE_READER_ALL_STREAMS"></a><a id="mf_source_reader_all_streams"></a><dl>
<dt><b>MF_SOURCE_READER_ALL_STREAMS</b></dt>
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There are two common uses for this method:

<ul>
<li>To change the default stream selection. Some media files contain multiple streams of the same type. For example, a file might include audio streams for multiple languages. You can use this method to change which of the streams is selected. To get information about each stream, call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute">IMFSourceReader::GetPresentationAttribute</a>  or <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype">IMFSourceReader::GetNativeMediaType</a>.</li>
<li>If you will not need data from one of the streams, it is a good idea to deselect that stream. If the stream is selected, the media source might hold onto a queue of unread data, and the queue might grow indefinitely, consuming memory. </li>
</ul>
For an example of deselecting a stream, see <a href="/windows/desktop/medfound/tutorial--decoding-audio">Tutorial: Decoding Audio</a>.

If a stream is deselected, the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a> method returns <b>MF_E_INVALIDREQUEST</b> for that stream. Other <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> methods are valid for deselected streams.

Stream selection does not affect how the source reader loads or unloads decoders in memory. In particular, deselecting a stream does not force the source reader to unload the decoder for that stream.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>