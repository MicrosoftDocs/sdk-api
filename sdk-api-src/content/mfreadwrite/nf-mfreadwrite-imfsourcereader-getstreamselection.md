---
UID: NF:mfreadwrite.IMFSourceReader.GetStreamSelection
title: IMFSourceReader::GetStreamSelection (mfreadwrite.h)
description: Queries whether a stream is selected.
old-location: mf\imfsourcereader_getstreamselection.htm
tech.root: medfound
ms.assetid: 40301426-4bf2-442c-91b5-9916d1314617
ms.date: 12/05/2018
ms.keywords: GetStreamSelection, GetStreamSelection method [Media Foundation], GetStreamSelection method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],GetStreamSelection method, IMFSourceReader.GetStreamSelection, IMFSourceReader::GetStreamSelection, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereader_getstreamselection, mfreadwrite/IMFSourceReader::GetStreamSelection
ms.topic: method
f1_keywords:
- mfreadwrite/IMFSourceReader.GetStreamSelection
dev_langs:
- c++
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
- IMFSourceReader.GetStreamSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceReader::GetStreamSelection


## -description


Queries whether a stream is selected.


## -parameters




### -param dwStreamIndex [in]

The stream to query. The value can be any of the following.

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
 


### -param pfSelected [out]

Receives <b>TRUE</b> if the stream is selected and will generate data. Receives <b>FALSE</b> if the stream is not selected and will not generate data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>
 

 

