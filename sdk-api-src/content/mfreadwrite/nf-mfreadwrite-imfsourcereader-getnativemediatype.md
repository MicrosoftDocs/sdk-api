---
UID: NF:mfreadwrite.IMFSourceReader.GetNativeMediaType
title: IMFSourceReader::GetNativeMediaType (mfreadwrite.h)
description: Gets a format that is supported natively by the media source.
helpviewer_keywords: ["GetNativeMediaType","GetNativeMediaType method [Media Foundation]","GetNativeMediaType method [Media Foundation]","IMFSourceReader interface","IMFSourceReader interface [Media Foundation]","GetNativeMediaType method","IMFSourceReader.GetNativeMediaType","IMFSourceReader::GetNativeMediaType","MF_SOURCE_READER_CURRENT_TYPE_INDEX","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","mf.imfsourcereader_getnativemediatype","mfreadwrite/IMFSourceReader::GetNativeMediaType"]
old-location: mf\imfsourcereader_getnativemediatype.htm
tech.root: mf
ms.assetid: 4b514f8d-082f-4e84-b512-d4a59706a6d8
ms.date: 12/05/2018
ms.keywords: GetNativeMediaType, GetNativeMediaType method [Media Foundation], GetNativeMediaType method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],GetNativeMediaType method, IMFSourceReader.GetNativeMediaType, IMFSourceReader::GetNativeMediaType, MF_SOURCE_READER_CURRENT_TYPE_INDEX, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereader_getnativemediatype, mfreadwrite/IMFSourceReader::GetNativeMediaType
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
 - IMFSourceReader::GetNativeMediaType
 - mfreadwrite/IMFSourceReader::GetNativeMediaType
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
 - IMFSourceReader.GetNativeMediaType
---

# IMFSourceReader::GetNativeMediaType


## -description

Gets a format that is supported natively by the media source.

## -parameters

### -param dwStreamIndex [in]

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

### -param dwMediaTypeIndex [in]

Specifies which media type to query. The value can be any of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0–0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
The zero-based index of a media type

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_CURRENT_TYPE_INDEX"></a><a id="mf_source_reader_current_type_index"></a><dl>
<dt><b>MF_SOURCE_READER_CURRENT_TYPE_INDEX</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The current native media type.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwMediaTypeIndex</i> parameter is out of range.

</td>
</tr>
</table>

## -remarks

This method queries the underlying media source for its native output format. Potentially, each source stream can produce more than one output format. Use the <i>dwMediaTypeIndex</i> parameter to loop through the available formats. Generally, file sources offer just one format per stream, but capture devices might offer several formats.

 The method returns a copy of the media type, so it is safe to modify the object received in the <i> ppMediaType</i> parameter.

To set  the output type for a stream, call the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">IMFSourceReader::SetCurrentMediaType</a> method.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>