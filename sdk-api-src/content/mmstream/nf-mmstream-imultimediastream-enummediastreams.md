---
UID: NF:mmstream.IMultiMediaStream.EnumMediaStreams
title: IMultiMediaStream::EnumMediaStreams (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The EnumMediaStreams method retrieves a media stream object, specified by index.
helpviewer_keywords: ["EnumMediaStreams","EnumMediaStreams method [DirectShow]","EnumMediaStreams method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","EnumMediaStreams method","IMultiMediaStream.EnumMediaStreams","IMultiMediaStream::EnumMediaStreams","IMultiMediaStreamEnumMediaStreams","dshow.imultimediastream_enummediastreams","mmstream/IMultiMediaStream::EnumMediaStreams"]
old-location: dshow\imultimediastream_enummediastreams.htm
tech.root: dshow
ms.assetid: 2fb51794-83ac-44c5-b388-d7b945870324
ms.date: 4/26/2023
ms.keywords: EnumMediaStreams, EnumMediaStreams method [DirectShow], EnumMediaStreams method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],EnumMediaStreams method, IMultiMediaStream.EnumMediaStreams, IMultiMediaStream::EnumMediaStreams, IMultiMediaStreamEnumMediaStreams, dshow.imultimediastream_enummediastreams, mmstream/IMultiMediaStream::EnumMediaStreams
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
 - IMultiMediaStream::EnumMediaStreams
 - mmstream/IMultiMediaStream::EnumMediaStreams
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
 - IMultiMediaStream.EnumMediaStreams
---

# IMultiMediaStream::EnumMediaStreams


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>EnumMediaStreams</code> method retrieves a media stream object, specified by index.

## -parameters

### -param Index [in]

Zero-based index of the media stream to retrieve.

### -param ppMediaStream [out]

Address of a variable that receives an <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> interface pointer.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Index is out of range.

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

If the return value is S_OK, the caller must release the <b>IMediaStream</b> interface.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>