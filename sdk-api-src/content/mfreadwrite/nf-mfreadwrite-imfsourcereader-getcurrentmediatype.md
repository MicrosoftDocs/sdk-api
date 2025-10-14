---
UID: NF:mfreadwrite.IMFSourceReader.GetCurrentMediaType
title: IMFSourceReader::GetCurrentMediaType (mfreadwrite.h)
description: Gets the current media type for a stream.
helpviewer_keywords: ["GetCurrentMediaType","GetCurrentMediaType method [Media Foundation]","GetCurrentMediaType method [Media Foundation]","IMFSourceReader interface","IMFSourceReader interface [Media Foundation]","GetCurrentMediaType method","IMFSourceReader.GetCurrentMediaType","IMFSourceReader::GetCurrentMediaType","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","mf.imfsourcereader_getcurrentmediatype","mfreadwrite/IMFSourceReader::GetCurrentMediaType"]
old-location: mf\imfsourcereader_getcurrentmediatype.htm
tech.root: mf
ms.assetid: c0fe3b34-42ad-45e4-812d-679bbe01a200
ms.date: 12/05/2018
ms.keywords: GetCurrentMediaType, GetCurrentMediaType method [Media Foundation], GetCurrentMediaType method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],GetCurrentMediaType method, IMFSourceReader.GetCurrentMediaType, IMFSourceReader::GetCurrentMediaType, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereader_getcurrentmediatype, mfreadwrite/IMFSourceReader::GetCurrentMediaType
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
 - IMFSourceReader::GetCurrentMediaType
 - mfreadwrite/IMFSourceReader::GetCurrentMediaType
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
 - IMFSourceReader.GetCurrentMediaType
---

# IMFSourceReader::GetCurrentMediaType


## -description

Gets the current media type for a stream.

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

### -param ppMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

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

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>