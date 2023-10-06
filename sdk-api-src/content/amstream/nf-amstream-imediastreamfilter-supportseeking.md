---
UID: NF:amstream.IMediaStreamFilter.SupportSeeking
title: IMediaStreamFilter::SupportSeeking (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SupportSeeking method initializes the filter to support seeking. The multimedia stream object calls this method.
helpviewer_keywords: ["IMediaStreamFilter interface [DirectShow]","SupportSeeking method","IMediaStreamFilter.SupportSeeking","IMediaStreamFilter::SupportSeeking","IMediaStreamFilterSupportSeeking","SupportSeeking","SupportSeeking method [DirectShow]","SupportSeeking method [DirectShow]","IMediaStreamFilter interface","amstream/IMediaStreamFilter::SupportSeeking","dshow.imediastreamfilter_supportseeking"]
old-location: dshow\imediastreamfilter_supportseeking.htm
tech.root: dshow
ms.assetid: 7cb15898-8a22-4621-a6e5-bb5d17640749
ms.date: 4/26/2023
ms.keywords: IMediaStreamFilter interface [DirectShow],SupportSeeking method, IMediaStreamFilter.SupportSeeking, IMediaStreamFilter::SupportSeeking, IMediaStreamFilterSupportSeeking, SupportSeeking, SupportSeeking method [DirectShow], SupportSeeking method [DirectShow],IMediaStreamFilter interface, amstream/IMediaStreamFilter::SupportSeeking, dshow.imediastreamfilter_supportseeking
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
 - IMediaStreamFilter::SupportSeeking
 - amstream/IMediaStreamFilter::SupportSeeking
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
 - IMediaStreamFilter.SupportSeeking
---

# IMediaStreamFilter::SupportSeeking


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SupportSeeking</code> method initializes the filter to support seeking. The multimedia stream object calls this method.

## -parameters

### -param bRenderer [in]

Boolean value that specifies whether the streams are being rendered. Use the value <b>TRUE</b> if the stream type is STREAMTYPE_READ, or <b>FALSE</b> otherwise.

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
The graph does not contain any seekable streams.

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

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>