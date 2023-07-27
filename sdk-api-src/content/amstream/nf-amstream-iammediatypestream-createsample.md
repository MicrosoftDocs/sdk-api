---
UID: NF:amstream.IAMMediaTypeStream.CreateSample
title: IAMMediaTypeStream::CreateSample (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The CreateSample method creates a stream sample and optionally specifies the sample buffer.
helpviewer_keywords: ["CreateSample","CreateSample method [DirectShow]","CreateSample method [DirectShow]","IAMMediaTypeStream interface","IAMMediaTypeStream interface [DirectShow]","CreateSample method","IAMMediaTypeStream.CreateSample","IAMMediaTypeStream::CreateSample","IAMMediaTypeStreamCreateSample","amstream/IAMMediaTypeStream::CreateSample","dshow.iammediatypestream_createsample"]
old-location: dshow\iammediatypestream_createsample.htm
tech.root: dshow
ms.assetid: 5bfdbf82-c298-498d-84e4-cd4d8cd13f82
ms.date: 4/26/2023
ms.keywords: CreateSample, CreateSample method [DirectShow], CreateSample method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],CreateSample method, IAMMediaTypeStream.CreateSample, IAMMediaTypeStream::CreateSample, IAMMediaTypeStreamCreateSample, amstream/IAMMediaTypeStream::CreateSample, dshow.iammediatypestream_createsample
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAMMediaTypeStream::CreateSample
 - amstream/IAMMediaTypeStream::CreateSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream.CreateSample
---

# IAMMediaTypeStream::CreateSample


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>CreateSample</code> method creates a stream sample and optionally specifies the sample buffer.

## -parameters

### -param lSampleSize [in]

Size of the sample.

### -param pbBuffer [in]

[optional] Pointer to an array of bytes that contains the sample data, or <b>NULL</b>.

### -param dwFlags [in]

Reserved.

### -param pUnkOuter [in]

[optional] Pointer to the interface of an object that aggregates the stream sample.

### -param ppAMMediaTypeSample [in]

Address of an <a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample</a> interface pointer that receives a pointer to the created sample.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>

## -remarks

If <i>pUnkOuter</i> is non-<b>NULL</b>, the new stream sample is aggregated into the specified object. Filters that receive the sample can then query it for interfaces supported by the aggregating object.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypestream">IAMMediaTypeStream Interface</a>