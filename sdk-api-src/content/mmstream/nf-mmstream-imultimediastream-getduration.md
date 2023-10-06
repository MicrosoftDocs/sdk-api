---
UID: NF:mmstream.IMultiMediaStream.GetDuration
title: IMultiMediaStream::GetDuration (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetDuration method retrieves the duration of the multimedia stream.
helpviewer_keywords: ["GetDuration","GetDuration method [DirectShow]","GetDuration method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetDuration method","IMultiMediaStream.GetDuration","IMultiMediaStream::GetDuration","IMultiMediaStreamGetDuration","dshow.imultimediastream_getduration","mmstream/IMultiMediaStream::GetDuration"]
old-location: dshow\imultimediastream_getduration.htm
tech.root: dshow
ms.assetid: 4d8104ec-aa2a-4151-bb7f-53611d4a71f2
ms.date: 4/26/2023
ms.keywords: GetDuration, GetDuration method [DirectShow], GetDuration method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetDuration method, IMultiMediaStream.GetDuration, IMultiMediaStream::GetDuration, IMultiMediaStreamGetDuration, dshow.imultimediastream_getduration, mmstream/IMultiMediaStream::GetDuration
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
 - IMultiMediaStream::GetDuration
 - mmstream/IMultiMediaStream::GetDuration
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
 - IMultiMediaStream.GetDuration
---

# IMultiMediaStream::GetDuration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetDuration</code> method retrieves the duration of the multimedia stream.

## -parameters

### -param pDuration [out]

Pointer to a variable that receives of the multimedia stream, in 100-nanosecond units.

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
This multimedia stream does not support seeking.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_INVALIDSTREAMTYPE</b></dt>
</dl>
</td>
<td width="60%">
This multimedia stream is not read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not determine the duration.

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