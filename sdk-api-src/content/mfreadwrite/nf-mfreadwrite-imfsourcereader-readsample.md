---
UID: NF:mfreadwrite.IMFSourceReader.ReadSample
title: IMFSourceReader::ReadSample (mfreadwrite.h)
description: Reads the next sample from the media source.
helpviewer_keywords: ["IMFSourceReader interface [Media Foundation]","ReadSample method","IMFSourceReader.ReadSample","IMFSourceReader::ReadSample","MF_SOURCE_READER_ANY_STREAM","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","ReadSample","ReadSample method [Media Foundation]","ReadSample method [Media Foundation]","IMFSourceReader interface","mf.imfsourcereader_readsample","mfreadwrite/IMFSourceReader::ReadSample"]
old-location: mf\imfsourcereader_readsample.htm
tech.root: mf
ms.assetid: 99bd9bd7-d8d1-433a-bc5a-4b9761de5048
ms.date: 12/05/2018
ms.keywords: IMFSourceReader interface [Media Foundation],ReadSample method, IMFSourceReader.ReadSample, IMFSourceReader::ReadSample, MF_SOURCE_READER_ANY_STREAM, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, ReadSample, ReadSample method [Media Foundation], ReadSample method [Media Foundation],IMFSourceReader interface, mf.imfsourcereader_readsample, mfreadwrite/IMFSourceReader::ReadSample
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
 - IMFSourceReader::ReadSample
 - mfreadwrite/IMFSourceReader::ReadSample
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
 - IMFSourceReader.ReadSample
---

# IMFSourceReader::ReadSample


## -description

Reads the next sample from the media source.

## -parameters

### -param dwStreamIndex [in]

The stream to pull data from. The value can be any of the following.

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
<td width="40%"><a id="MF_SOURCE_READER_ANY_STREAM"></a><a id="mf_source_reader_any_stream"></a><dl>
<dt><b>MF_SOURCE_READER_ANY_STREAM</b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
Get the next available sample, regardless of which stream.

</td>
</tr>
</table>

### -param dwControlFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag">MF_SOURCE_READER_CONTROL_FLAG</a> enumeration.

### -param pdwActualStreamIndex [out]

Receives the zero-based index of the stream.

### -param pdwStreamFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag">MF_SOURCE_READER_FLAG</a> enumeration.

### -param pllTimestamp [out]

Receives the time stamp of the sample, or the time of the stream event indicated in <i>pdwStreamFlags</i>. The time is given in 100-nanosecond units.

### -param ppSample [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface or the value <b>NULL</b> (see Remarks). If this parameter receives a non-<b>NULL</b> pointer, the caller must release the interface.

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
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
A flush operation is pending. See <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush">IMFSourceReader::Flush</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. See Remarks.

</td>
</tr>
</table>

## -remarks

If the requested stream is not selected, the return code is <b>MF_E_INVALIDREQUEST</b>. See <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection">IMFSourceReader::SetStreamSelection</a>.

 This method can complete synchronously or asynchronously. If you provide a callback pointer when you create the source reader, the method is asynchronous. Otherwise, the method is synchronous. For more information about setting the callback pointer, see <a href="/windows/desktop/medfound/mf-source-reader-async-callback">MF_SOURCE_READER_ASYNC_CALLBACK</a>.

<h3><a id="Asynchronous_Mode"></a><a id="asynchronous_mode"></a><a id="ASYNCHRONOUS_MODE"></a>Asynchronous Mode</h3>
In asynchronous mode:

<ul>
<li>All of the <code>[out]</code> parameters must be <b>NULL</b>. Otherwise, the method returns <b>E_INVALIDARG</b>.</li>
<li>The method returns immediately.</li>
<li>When the operation completes, the application's <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample">IMFSourceReaderCallback::OnReadSample</a> method is called.</li>
<li>If an error occurs, the method can fail either synchronously or asynchronously. Check the return value of <b>ReadSample</b>, and also check the <i>hrStatus</i> parameter of <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample">IMFSourceReaderCallback::OnReadSample</a>.</li>
</ul>
<h3><a id="Synchronous_Mode"></a><a id="synchronous_mode"></a><a id="SYNCHRONOUS_MODE"></a>Synchronous Mode</h3>
In synchronous mode:

<ul>
<li>The <i>pdwStreamFlags</i> and <i>ppSample</i> parameters cannot be <b>NULL</b>. Otherwise, the method returns <b>E_POINTER</b>.</li>
<li>The <i>pdwActualStreamIndex</i> and <i>pllTimestamp</i> parameters can be <b>NULL</b>.</li>
<li>The method blocks until the next sample is available.</li>
</ul>
In synchronous mode, if the <i>dwStreamIndex</i> parameter is <b>MF_SOURCE_READER_ANY_STREAM</b>, you should pass a non-<b>NULL</b> value for <i>pdwActualStreamIndex</i>, so that you know which stream delivered the sample.

This method can return flags in the <i>pdwStreamFlags</i> parameter without returning a media sample in <i>ppSample</i>. Therefore, the <i>ppSample</i> parameter can receive a <b>NULL</b> pointer even when the method succeeds. For example, when the source reader reaches the end of the stream, it returns the <b>MF_SOURCE_READERF_ENDOFSTREAM</b> flag in <i>pdwStreamFlags</i> and sets <i>ppSample</i> to <b>NULL</b>.

If there is a gap in the stream, <i>pdwStreamFlags</i> receives the MF_SOURCE_READERF_STREAMTICK flag, <i>ppSample</i> is <b>NULL</b>, and <i>pllTimestamp</i> indicates the time when the gap occurred. 

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>