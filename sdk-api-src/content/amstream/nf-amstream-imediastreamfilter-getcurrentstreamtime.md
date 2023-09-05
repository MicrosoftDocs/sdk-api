---
UID: NF:amstream.IMediaStreamFilter.GetCurrentStreamTime
title: IMediaStreamFilter::GetCurrentStreamTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetCurrentStreamTime method retrieves the current stream time.
helpviewer_keywords: ["GetCurrentStreamTime","GetCurrentStreamTime method [DirectShow]","GetCurrentStreamTime method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","GetCurrentStreamTime method","IMediaStreamFilter.GetCurrentStreamTime","IMediaStreamFilter::GetCurrentStreamTime","IMediaStreamFilterGetCurrentStreamTime","amstream/IMediaStreamFilter::GetCurrentStreamTime","dshow.imediastreamfilter_getcurrentstreamtime"]
old-location: dshow\imediastreamfilter_getcurrentstreamtime.htm
tech.root: dshow
ms.assetid: 933f83a3-600e-4897-b4df-a481d2874155
ms.date: 4/26/2023
ms.keywords: GetCurrentStreamTime, GetCurrentStreamTime method [DirectShow], GetCurrentStreamTime method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],GetCurrentStreamTime method, IMediaStreamFilter.GetCurrentStreamTime, IMediaStreamFilter::GetCurrentStreamTime, IMediaStreamFilterGetCurrentStreamTime, amstream/IMediaStreamFilter::GetCurrentStreamTime, dshow.imediastreamfilter_getcurrentstreamtime
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
 - IMediaStreamFilter::GetCurrentStreamTime
 - amstream/IMediaStreamFilter::GetCurrentStreamTime
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
 - IMediaStreamFilter.GetCurrentStreamTime
---

# IMediaStreamFilter::GetCurrentStreamTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>GetCurrentStreamTime</b> method retrieves the current stream time.

## -parameters

### -param pCurrentStreamTime [out]

Pointer to a variable that receives the stream time, in 100-nanosecond units.

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
The graph is not running, or there is no reference clock.

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

Stream time is defined only when the graph is running and has a reference clock. Otherwise, *<i>pCurrentStreamTime</i> is set to zero and the method returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>