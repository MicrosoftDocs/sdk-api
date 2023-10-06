---
UID: NF:strmif.IMediaSeeking.GetCapabilities
title: IMediaSeeking::GetCapabilities (strmif.h)
description: The GetCapabilities method retrieves all the seeking capabilities of the stream.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [DirectShow]","GetCapabilities method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetCapabilities method","IMediaSeeking.GetCapabilities","IMediaSeeking::GetCapabilities","IMediaSeekingGetCapabilities","dshow.imediaseeking_getcapabilities","strmif/IMediaSeeking::GetCapabilities"]
old-location: dshow\imediaseeking_getcapabilities.htm
tech.root: dshow
ms.assetid: 84dd3c21-9c72-4433-bd03-29520dc138ca
ms.date: 4/26/2023
ms.keywords: GetCapabilities, GetCapabilities method [DirectShow], GetCapabilities method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetCapabilities method, IMediaSeeking.GetCapabilities, IMediaSeeking::GetCapabilities, IMediaSeekingGetCapabilities, dshow.imediaseeking_getcapabilities, strmif/IMediaSeeking::GetCapabilities
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaSeeking::GetCapabilities
 - strmif/IMediaSeeking::GetCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSeeking.GetCapabilities
---

# IMediaSeeking::GetCapabilities


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCapabilities</code> method retrieves all the seeking capabilities of the stream.

## -parameters

### -param pCapabilities [out]

Pointer to a variable that receives a bitwise combination of <a href="/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities">AM_SEEKING_SEEKING_CAPABILITIES</a> flags.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
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
</table>

## -remarks

This method returns information on all the seeking capabilities of the stream. Examine <i>pCapabilities</i> by performing a separate bitwise-AND operation on each AM_SEEKING_SEEKING_CAPABILITIES value you are interested in.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
DWORD dwCaps = 0;
pMediaSeeking-&gt;GetCapabilities(&amp;dwCaps);

if (dwCaps &amp; AM_SEEKING_CanGetCurrentPos) 
{
    // The stream can seek to the current position.
}
if (dwCaps &amp; AM_SEEKING_CanPlayBackwards) 
{
    // The stream can play backward.
}
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>

