---
UID: NF:mmstream.IMultiMediaStream.GetMediaStream
title: IMultiMediaStream::GetMediaStream (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetMediaStream method retrieves a media stream, specified by purpose ID.
helpviewer_keywords: ["GetMediaStream","GetMediaStream method [DirectShow]","GetMediaStream method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetMediaStream method","IMultiMediaStream.GetMediaStream","IMultiMediaStream::GetMediaStream","IMultiMediaStreamGetMediaStream","dshow.imultimediastream_getmediastream","mmstream/IMultiMediaStream::GetMediaStream"]
old-location: dshow\imultimediastream_getmediastream.htm
tech.root: dshow
ms.assetid: d85cde4f-99f4-4641-b75f-13ca6dc7f21e
ms.date: 4/26/2023
ms.keywords: GetMediaStream, GetMediaStream method [DirectShow], GetMediaStream method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetMediaStream method, IMultiMediaStream.GetMediaStream, IMultiMediaStream::GetMediaStream, IMultiMediaStreamGetMediaStream, dshow.imultimediastream_getmediastream, mmstream/IMultiMediaStream::GetMediaStream
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
 - IMultiMediaStream::GetMediaStream
 - mmstream/IMultiMediaStream::GetMediaStream
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
 - IMultiMediaStream.GetMediaStream
---

# IMultiMediaStream::GetMediaStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaStream</code> method retrieves a media stream, specified by purpose ID.

## -parameters

### -param idPurpose

Reference to an <a href="/windows/desktop/DirectShow/mspid">MSPID</a> that identifies the media stream to retrieve.

### -param ppMediaStream

Address of variable that receives an <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> interface pointer.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No matching stream.

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

If the method succeeds, the caller must release the <b>IMediaStream</b> interface.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>