---
UID: NF:amstream.IAMMediaTypeStream.GetFormat
title: IAMMediaTypeStream::GetFormat (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetFormat method retrieves the format of the stream.
helpviewer_keywords: ["GetFormat","GetFormat method [DirectShow]","GetFormat method [DirectShow]","IAMMediaTypeStream interface","IAMMediaTypeStream interface [DirectShow]","GetFormat method","IAMMediaTypeStream.GetFormat","IAMMediaTypeStream::GetFormat","IAMMediaTypeStreamGetFormat","amstream/IAMMediaTypeStream::GetFormat","dshow.iammediatypestream_getformat"]
old-location: dshow\iammediatypestream_getformat.htm
tech.root: dshow
ms.assetid: 9f00fe45-df4b-4787-980c-9fe434a8ab7e
ms.date: 4/26/2023
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],GetFormat method, IAMMediaTypeStream.GetFormat, IAMMediaTypeStream::GetFormat, IAMMediaTypeStreamGetFormat, amstream/IAMMediaTypeStream::GetFormat, dshow.iammediatypestream_getformat
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
 - IAMMediaTypeStream::GetFormat
 - amstream/IAMMediaTypeStream::GetFormat
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
 - IAMMediaTypeStream.GetFormat
---

# IAMMediaTypeStream::GetFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFormat</code> method retrieves the format of the stream.

## -parameters

### -param pMediaType [out]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that receives the stream format.

### -param dwFlags [in]

Reserved.

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
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No stream is associated with this object.

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

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypestream">IAMMediaTypeStream Interface</a>