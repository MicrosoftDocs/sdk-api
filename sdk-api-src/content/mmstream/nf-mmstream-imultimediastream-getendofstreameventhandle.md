---
UID: NF:mmstream.IMultiMediaStream.GetEndOfStreamEventHandle
title: IMultiMediaStream::GetEndOfStreamEventHandle (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetEndOfStreamEventHandle method retrieves an event that is signaled when the multimedia stream completes playback.
helpviewer_keywords: ["GetEndOfStreamEventHandle","GetEndOfStreamEventHandle method [DirectShow]","GetEndOfStreamEventHandle method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetEndOfStreamEventHandle method","IMultiMediaStream.GetEndOfStreamEventHandle","IMultiMediaStream::GetEndOfStreamEventHandle","IMultiMediaStreamGetEndOfStreamEventHandle","dshow.imultimediastream_getendofstreameventhandle","mmstream/IMultiMediaStream::GetEndOfStreamEventHandle"]
old-location: dshow\imultimediastream_getendofstreameventhandle.htm
tech.root: dshow
ms.assetid: 0e4f59f8-c56e-4768-9047-2793515edfeb
ms.date: 4/26/2023
ms.keywords: GetEndOfStreamEventHandle, GetEndOfStreamEventHandle method [DirectShow], GetEndOfStreamEventHandle method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetEndOfStreamEventHandle method, IMultiMediaStream.GetEndOfStreamEventHandle, IMultiMediaStream::GetEndOfStreamEventHandle, IMultiMediaStreamGetEndOfStreamEventHandle, dshow.imultimediastream_getendofstreameventhandle, mmstream/IMultiMediaStream::GetEndOfStreamEventHandle
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
 - IMultiMediaStream::GetEndOfStreamEventHandle
 - mmstream/IMultiMediaStream::GetEndOfStreamEventHandle
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
 - IMultiMediaStream.GetEndOfStreamEventHandle
---

# IMultiMediaStream::GetEndOfStreamEventHandle


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetEndOfStreamEventHandle</code> method retrieves an event that is signaled when the multimedia stream completes playback.

## -parameters

### -param phEOS [out]

Pointer to a variable that receives a handle to the event. The event is signaled when all of the streams in the multimedia stream object complete playback.

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
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The multimedia stream is not stopped.

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

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>