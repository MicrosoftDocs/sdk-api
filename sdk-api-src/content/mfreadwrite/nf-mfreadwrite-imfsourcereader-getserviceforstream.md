---
UID: NF:mfreadwrite.IMFSourceReader.GetServiceForStream
title: IMFSourceReader::GetServiceForStream (mfreadwrite.h)
description: Queries the underlying media source or decoder for an interface.
helpviewer_keywords: ["GetServiceForStream","GetServiceForStream method [Media Foundation]","GetServiceForStream method [Media Foundation]","IMFSourceReader interface","IMFSourceReader interface [Media Foundation]","GetServiceForStream method","IMFSourceReader.GetServiceForStream","IMFSourceReader::GetServiceForStream","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","MF_SOURCE_READER_MEDIASOURCE","mf.imfsourcereader_getserviceforstream","mfreadwrite/IMFSourceReader::GetServiceForStream"]
old-location: mf\imfsourcereader_getserviceforstream.htm
tech.root: mf
ms.assetid: d8868e4d-eedd-4fbd-b870-d3af48890c92
ms.date: 12/05/2018
ms.keywords: GetServiceForStream, GetServiceForStream method [Media Foundation], GetServiceForStream method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],GetServiceForStream method, IMFSourceReader.GetServiceForStream, IMFSourceReader::GetServiceForStream, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, MF_SOURCE_READER_MEDIASOURCE, mf.imfsourcereader_getserviceforstream, mfreadwrite/IMFSourceReader::GetServiceForStream
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
 - IMFSourceReader::GetServiceForStream
 - mfreadwrite/IMFSourceReader::GetServiceForStream
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
 - IMFSourceReader.GetServiceForStream
---

# IMFSourceReader::GetServiceForStream


## -description

Queries the underlying media source or decoder for an interface.

## -parameters

### -param dwStreamIndex [in]

The stream or object to query. If the value is <b>MF_SOURCE_READER_MEDIASOURCE</b>, the method queries the media source. Otherwise, it queries the decoder that is associated with the specified stream. The following values are possible.

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
<td width="40%"><a id="MF_SOURCE_READER_MEDIASOURCE"></a><a id="mf_source_reader_mediasource"></a><dl>
<dt><b>MF_SOURCE_READER_MEDIASOURCE</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The media source.


</td>
</tr>
</table>

### -param guidService [in]

A service identifier GUID.  If the value is <b>GUID_NULL</b>, the method calls <b>QueryInterface</b> to get the requested interface. Otherwise, the method calls the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method. For a list of service identifiers, see <a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>