---
UID: NF:ddstream.IDirectDrawMediaStream.CreateSample
title: IDirectDrawMediaStream::CreateSample (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Creates a stream sample using the specified DirectDraw surface object.
helpviewer_keywords: ["CreateSample","CreateSample method [DirectShow]","CreateSample method [DirectShow]","IDirectDrawMediaStream interface","IDirectDrawMediaStream interface [DirectShow]","CreateSample method","IDirectDrawMediaStream.CreateSample","IDirectDrawMediaStream::CreateSample","IDirectDrawMediaStreamCreateSample","ddstream/IDirectDrawMediaStream::CreateSample","dshow.idirectdrawmediastream_createsample"]
old-location: dshow\idirectdrawmediastream_createsample.htm
tech.root: dshow
ms.assetid: 85041c71-f9fc-48fc-8fe2-fec21efb831b
ms.date: 4/26/2023
ms.keywords: CreateSample, CreateSample method [DirectShow], CreateSample method [DirectShow],IDirectDrawMediaStream interface, IDirectDrawMediaStream interface [DirectShow],CreateSample method, IDirectDrawMediaStream.CreateSample, IDirectDrawMediaStream::CreateSample, IDirectDrawMediaStreamCreateSample, ddstream/IDirectDrawMediaStream::CreateSample, dshow.idirectdrawmediastream_createsample
req.header: ddstream.h
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
 - IDirectDrawMediaStream::CreateSample
 - ddstream/IDirectDrawMediaStream::CreateSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawMediaStream.CreateSample
---

# IDirectDrawMediaStream::CreateSample


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Creates a stream sample using the specified DirectDraw surface object.

## -parameters

### -param pSurface [in]

Pointer to an existing DirectDraw surface. Use <b>QueryInterface</b> to obtain the <b>IDirectDrawSurface</b> interface from an <b>IDirectDrawSurface7</b> interface pointer.

### -param pRect [in]

Pointer to the clipping rectangle you want to use with the specified surface. Set this parameter to <b>NULL</b> if you want to use the entire surface.

### -param dwFlags [in]

Specifies miscellaneous flags. The following flag is defined:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DDSFF_PROGRESSIVERENDER</td>
<td>If this flag is set, sample updates are performed directly on the surface. When this flag is absent, if the decoder uses delta frames, an extra copy is performed internally. Setting this flag can improve performance but can also introduce tearing.</td>
</tr>
</table>

### -param ppSample [out]

Address of a pointer to an <a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample">IDirectDrawStreamSample</a> interface that will point to the newly created sample.

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
<dt><b>DDERR_INVALIDPIXELFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The specified pixel format is incompatible with the stream format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
The specified clipping rectangle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDSURFACETYPE</b></dt>
</dl>
</td>
<td width="60%">
The specified surface is incompatible with the stream format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the required parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_SAMPLEALLOC</b></dt>
</dl>
</td>
<td width="60%">
The stream already has allocated samples and the surface doesn't match the sample format.

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

This method creates a sample from the current stream and attaches the sample to this surface.

If the stream doesn't have an allocated surface and the specified surface doesn't match the stream's format, this method calls the <a href="/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-setformat">IDirectDrawMediaStream::SetFormat</a> method on the stream so the two will match.

To perform a progressive render, create a single sample and repeatedly use that sample for successive frames of video. Video decompressors use this technique to do partial updates to the previous frame.

The <i>pRect</i> parameter should match the format of the stream (see <a href="/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-getformat">IDirectDrawMediaStream::GetFormat</a>). If the wrong clip rectangle is set or no clip rectangle is set, and the surface size does not match the movie size, the movie might not play. If a primary surface is used, it is advisable to use a clipping rectangle because the primary surface size can change if the user changes display settings.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>