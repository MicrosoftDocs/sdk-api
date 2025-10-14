---
UID: NF:mfreadwrite.IMFSourceReaderEx.GetTransformForStream
title: IMFSourceReaderEx::GetTransformForStream (mfreadwrite.h)
description: Gets a pointer to a Media Foundation transform (MFT) for a specified stream. (IMFSourceReaderEx.GetTransformForStream)
helpviewer_keywords: ["GetTransformForStream","GetTransformForStream method [Media Foundation]","GetTransformForStream method [Media Foundation]","IMFSourceReaderEx interface","IMFSourceReaderEx interface [Media Foundation]","GetTransformForStream method","IMFSourceReaderEx.GetTransformForStream","IMFSourceReaderEx::GetTransformForStream","MF_SOURCE_READER_FIRST_AUDIO_STREAM","MF_SOURCE_READER_FIRST_VIDEO_STREAM","mf.imfsourcereaderex_gettransformforstream","mfreadwrite/IMFSourceReaderEx::GetTransformForStream"]
old-location: mf\imfsourcereaderex_gettransformforstream.htm
tech.root: mf
ms.assetid: 39F2D132-5D2B-4389-AB30-FE2942EC3965
ms.date: 12/05/2018
ms.keywords: GetTransformForStream, GetTransformForStream method [Media Foundation], GetTransformForStream method [Media Foundation],IMFSourceReaderEx interface, IMFSourceReaderEx interface [Media Foundation],GetTransformForStream method, IMFSourceReaderEx.GetTransformForStream, IMFSourceReaderEx::GetTransformForStream, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereaderex_gettransformforstream, mfreadwrite/IMFSourceReaderEx::GetTransformForStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceReaderEx::GetTransformForStream
 - mfreadwrite/IMFSourceReaderEx::GetTransformForStream
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
 - IMFSourceReaderEx.GetTransformForStream
---

# IMFSourceReaderEx::GetTransformForStream


## -description

Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

## -parameters

### -param dwStreamIndex [in]

The stream to query for the MFT. The value can be any of the following.

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

### -param dwTransformIndex [in]

The zero-based index of the MFT to retrieve.

### -param pGuidCategory [out]

Receives a GUID that specifies the category of the MFT. For a list of possible values, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -param ppTransform [out]

Receives a pointer to the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface of the MFT. The caller must release the interface.

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
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransformIndex</i> parameter is out of range.

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

You can use this method to configure an MFT after it is inserted into the processing chain. Do not use the pointer returned in <i>ppTransform</i> to set media types on the MFT or to process data. In particular, calling any of the following <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> methods could have unexpected results.

<ul>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams">AddInputStreams</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream">DeleteInputStream</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent">ProcessEvent</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">ProcessInput</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">ProcessMessage</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype">SetInputType</a>
</li>
<li>
<a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype">SetOutputType</a>
</li>
</ul>
If a decoder is present, it appears at index position zero.

To avoid losing any data, you should drain the source reader before calling this method. For more information, see <a href="/windows/desktop/medfound/processing-media-data-with-the-source-reader">Draining the Data Pipeline</a>.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex">IMFSourceReaderEx</a>
