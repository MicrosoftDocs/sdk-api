---
UID: NF:strmif.IMediaSample.GetMediaType
title: IMediaSample::GetMediaType (strmif.h)
description: The GetMediaType method retrieves the media type, if the media type differs from the previous sample.
helpviewer_keywords: ["GetMediaType","GetMediaType method [DirectShow]","GetMediaType method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetMediaType method","IMediaSample.GetMediaType","IMediaSample::GetMediaType","IMediaSampleGetMediaType","dshow.imediasample_getmediatype","strmif/IMediaSample::GetMediaType"]
old-location: dshow\imediasample_getmediatype.htm
tech.root: dshow
ms.assetid: abccec09-c5a0-4192-9bdf-9240d1b73357
ms.date: 4/26/2023
ms.keywords: GetMediaType, GetMediaType method [DirectShow], GetMediaType method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetMediaType method, IMediaSample.GetMediaType, IMediaSample::GetMediaType, IMediaSampleGetMediaType, dshow.imediasample_getmediatype, strmif/IMediaSample::GetMediaType
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaSample::GetMediaType
 - strmif/IMediaSample::GetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample.GetMediaType
---

# IMediaSample::GetMediaType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMediaType</code> method retrieves the media type, if the media type differs from the previous sample.

## -parameters

### -param ppMediaType

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure. If the media type has not changed from the previous sample, <i>*ppMediaType</i> is set to <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The media type has not changed from the previous sample.

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
</table>

## -remarks

This method enables a filter to make limited changes to the media type, such as changing the palette. To make a significant change to the media type, the pins might need to reconnect and renegotiate the media type.

If the method returns S_OK, the caller must free the memory for the media type, including the format block. You can use the <a href="/windows/desktop/DirectShow/deletemediatype">DeleteMediaType</a> function in the DirectShow base class library.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>