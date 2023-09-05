---
UID: NF:ddstream.IDirectDrawMediaStream.SetFormat
title: IDirectDrawMediaStream::SetFormat (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Sets the format of the current media stream.
helpviewer_keywords: ["IDirectDrawMediaStream interface [DirectShow]","SetFormat method","IDirectDrawMediaStream.SetFormat","IDirectDrawMediaStream::SetFormat","IDirectDrawMediaStreamSetFormat","SetFormat","SetFormat method [DirectShow]","SetFormat method [DirectShow]","IDirectDrawMediaStream interface","ddstream/IDirectDrawMediaStream::SetFormat","dshow.idirectdrawmediastream_setformat"]
old-location: dshow\idirectdrawmediastream_setformat.htm
tech.root: dshow
ms.assetid: 465b4f0c-40e1-4aec-be62-0b55c29fa05e
ms.date: 4/26/2023
ms.keywords: IDirectDrawMediaStream interface [DirectShow],SetFormat method, IDirectDrawMediaStream.SetFormat, IDirectDrawMediaStream::SetFormat, IDirectDrawMediaStreamSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IDirectDrawMediaStream interface, ddstream/IDirectDrawMediaStream::SetFormat, dshow.idirectdrawmediastream_setformat
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
 - IDirectDrawMediaStream::SetFormat
 - ddstream/IDirectDrawMediaStream::SetFormat
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
 - IDirectDrawMediaStream.SetFormat
---

# IDirectDrawMediaStream::SetFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the format of the current media stream.

## -parameters

### -param pDDSurfaceDesc [in]

Pointer to a DirectDraw surface description that contains the new format.

### -param pDirectDrawPalette [in]

Optional parameter that is a pointer to an <b>IDirectDrawPalette</b> interface.

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
<dt><b>DDERR_INVALIDSURFACETYPE</b></dt>
</dl>
</td>
<td width="60%">
The specified format is incompatible with the current stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_SAMPLEALLOC</b></dt>
</dl>
</td>
<td width="60%">
Can't change the format because one or more stream samples are already allocated for this stream.

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

If the stream already has allocated samples and the sample format doesn't match the specified format, this method fails. This method always succeeds if the specified format matches the current format.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>