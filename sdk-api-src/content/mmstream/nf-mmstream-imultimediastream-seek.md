---
UID: NF:mmstream.IMultiMediaStream.Seek
title: IMultiMediaStream::Seek (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The Seek method seeks all of the media streams to a new position.
helpviewer_keywords: ["IMultiMediaStream interface [DirectShow]","Seek method","IMultiMediaStream.Seek","IMultiMediaStream::Seek","IMultiMediaStreamSeek","Seek","Seek method [DirectShow]","Seek method [DirectShow]","IMultiMediaStream interface","dshow.imultimediastream_seek","mmstream/IMultiMediaStream::Seek"]
old-location: dshow\imultimediastream_seek.htm
tech.root: dshow
ms.assetid: ac65613f-3fca-4043-83ad-740ebd7687a4
ms.date: 4/26/2023
ms.keywords: IMultiMediaStream interface [DirectShow],Seek method, IMultiMediaStream.Seek, IMultiMediaStream::Seek, IMultiMediaStreamSeek, Seek, Seek method [DirectShow], Seek method [DirectShow],IMultiMediaStream interface, dshow.imultimediastream_seek, mmstream/IMultiMediaStream::Seek
req.header: mmstream.h
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
 - IMultiMediaStream::Seek
 - mmstream/IMultiMediaStream::Seek
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream.Seek
---

# IMultiMediaStream::Seek


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Seek</code> method seeks all of the media streams to a new position.

## -parameters

### -param SeekTime [in]

<a href="/windows/desktop/DirectShow/stream-time">STREAM_TIME</a> value that specifies the new position.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The media streams do not support seeking.

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

To determine whether the media streams support seeking, call the <a href="/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getinformation">IMultiMediaStream::GetInformation</a> method.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>