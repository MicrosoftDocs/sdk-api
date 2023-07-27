---
UID: NF:amstream.IMediaStreamFilter.WaitUntil
title: IMediaStreamFilter::WaitUntil (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The WaitUntil method causes the filter to block until a specified stream time. The filter's pins call this method. They can interrupt the wait by flushing the filter.
helpviewer_keywords: ["IMediaStreamFilter interface [DirectShow]","WaitUntil method","IMediaStreamFilter.WaitUntil","IMediaStreamFilter::WaitUntil","IMediaStreamFilterWaitUntil","WaitUntil","WaitUntil method [DirectShow]","WaitUntil method [DirectShow]","IMediaStreamFilter interface","amstream/IMediaStreamFilter::WaitUntil","dshow.imediastreamfilter_waituntil"]
old-location: dshow\imediastreamfilter_waituntil.htm
tech.root: dshow
ms.assetid: 5669a3c6-b060-49e8-b8e6-2e3617b44d62
ms.date: 4/26/2023
ms.keywords: IMediaStreamFilter interface [DirectShow],WaitUntil method, IMediaStreamFilter.WaitUntil, IMediaStreamFilter::WaitUntil, IMediaStreamFilterWaitUntil, WaitUntil, WaitUntil method [DirectShow], WaitUntil method [DirectShow],IMediaStreamFilter interface, amstream/IMediaStreamFilter::WaitUntil, dshow.imediastreamfilter_waituntil
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
 - IMediaStreamFilter::WaitUntil
 - amstream/IMediaStreamFilter::WaitUntil
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
 - IMediaStreamFilter.WaitUntil
---

# IMediaStreamFilter::WaitUntil


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>WaitUntil</b> method causes the filter to block until a specified stream time. The filter's pins call this method. They can interrupt the wait by flushing the filter.

## -parameters

### -param WaitStreamTime [in]

Specifies the stream time, in 100-nanosecond units.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The wait was interrupted.

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

If the graph does not have a reference clock, the method returns E_FAIL.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>