---
UID: NF:mfreadwrite.IMFSourceReaderEx.SetNativeMediaType
title: IMFSourceReaderEx::SetNativeMediaType (mfreadwrite.h)
description: Sets the native media type for a stream on the media source.
helpviewer_keywords: ["IMFSourceReaderEx interface [Media Foundation]","SetNativeMediaType method","IMFSourceReaderEx.SetNativeMediaType","IMFSourceReaderEx::SetNativeMediaType","MF_SOURCE_READERF_ALLEFFECTSREMOVED","MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED","SetNativeMediaType","SetNativeMediaType method [Media Foundation]","SetNativeMediaType method [Media Foundation]","IMFSourceReaderEx interface","mf.imfsourcereaderex_setnativemediatype","mfreadwrite/IMFSourceReaderEx::SetNativeMediaType"]
old-location: mf\imfsourcereaderex_setnativemediatype.htm
tech.root: mf
ms.assetid: 532E8F28-16F4-442E-83D9-C247E8FA7E2A
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderEx interface [Media Foundation],SetNativeMediaType method, IMFSourceReaderEx.SetNativeMediaType, IMFSourceReaderEx::SetNativeMediaType, MF_SOURCE_READERF_ALLEFFECTSREMOVED, MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED, SetNativeMediaType, SetNativeMediaType method [Media Foundation], SetNativeMediaType method [Media Foundation],IMFSourceReaderEx interface, mf.imfsourcereaderex_setnativemediatype, mfreadwrite/IMFSourceReaderEx::SetNativeMediaType
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
 - IMFSourceReaderEx::SetNativeMediaType
 - mfreadwrite/IMFSourceReaderEx::SetNativeMediaType
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
 - IMFSourceReaderEx.SetNativeMediaType
---

# IMFSourceReaderEx::SetNativeMediaType


## -description

Sets the native media type for a stream on the media source.

## -parameters

### -param dwStreamIndex [in]

### -param pMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type.

### -param pdwStreamFlags [out]

Receives a bitwise <b>OR</b> of zero or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READERF_ALLEFFECTSREMOVED"></a><a id="mf_source_readerf_alleffectsremoved"></a><dl>
<dt><b>MF_SOURCE_READERF_ALLEFFECTSREMOVED</b></dt>
</dl>
</td>
<td width="60%">
All effects were removed from the stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED"></a><a id="mf_source_readerf_currentmediatypechanged"></a><dl>
<dt><b>MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED</b></dt>
</dl>
</td>
<td width="60%">
The current output type changed.

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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

This method sets the output type that is produced by the media source. Unlike the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">IMFSourceReader::SetCurrentMediaType</a> method, this method does not insert any decoders, video processors, or other transforms. The media source must support the specified media type natively. To get a list of supported types from the media source, call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype">IMFSourceReader::GetNativeMediaType</a>.

In asynchronous mode, this method fails if a sample request is pending. In that case, wait for the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample">OnReadSample</a> callback to be invoked before calling the method. For more information about using the Source Reader in asynchronous mode, see <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a>.

This method can trigger a change in the output format for the stream. If so, the <b>MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED</b> flag is returned in the  <i>pdwStreamFlags</i> parameter. The method might also cause the Source Reader to remove any effects that were added by the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereaderex-addtransformforstream">IMFSourceReaderEx::AddTransformForStream</a> method. If this occurs, the  <b>MF_SOURCE_READERF_ALLEFFECTSREMOVED</b> flag is returned in <i>pdwStreamFlags</i>. 

This method is useful with audio and video capture devices, because a device might support several output formats. This method enables the application to choose the device format before decoders and other transforms are added.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex">IMFSourceReaderEx</a>