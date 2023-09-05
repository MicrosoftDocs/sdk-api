---
UID: NF:amstream.IAMMultiMediaStream.GetFilter
title: IAMMultiMediaStream::GetFilter (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetFilter method retrieves the Media Stream filter, which is used internally by the multimedia stream object.
helpviewer_keywords: ["GetFilter","GetFilter method [DirectShow]","GetFilter method [DirectShow]","IAMMultiMediaStream interface","IAMMultiMediaStream interface [DirectShow]","GetFilter method","IAMMultiMediaStream.GetFilter","IAMMultiMediaStream::GetFilter","IAMMultiMediaStreamGetFilter","amstream/IAMMultiMediaStream::GetFilter","dshow.iammultimediastream_getfilter"]
old-location: dshow\iammultimediastream_getfilter.htm
tech.root: dshow
ms.assetid: 7e4df9cb-4008-4615-a179-ae1e76c22337
ms.date: 4/26/2023
ms.keywords: GetFilter, GetFilter method [DirectShow], GetFilter method [DirectShow],IAMMultiMediaStream interface, IAMMultiMediaStream interface [DirectShow],GetFilter method, IAMMultiMediaStream.GetFilter, IAMMultiMediaStream::GetFilter, IAMMultiMediaStreamGetFilter, amstream/IAMMultiMediaStream::GetFilter, dshow.iammultimediastream_getfilter
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
 - IAMMultiMediaStream::GetFilter
 - amstream/IAMMultiMediaStream::GetFilter
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
 - IAMMultiMediaStream.GetFilter
---

# IAMMultiMediaStream::GetFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFilter</code> method retrieves the Media Stream filter, which is used internally by the multimedia stream object.

## -parameters

### -param ppFilter [out]

Address of a variable that receives an <a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter</a> interface pointer.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

Applications should not call this method. The <b>IMediaStreamFilter</b> interface is not intended for applications to use.

If the method succeeds, the caller must release the <b>IMediaStreamFilter</b> interface.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>