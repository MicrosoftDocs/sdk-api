---
UID: NF:strmif.IMediaSeeking.CheckCapabilities
title: IMediaSeeking::CheckCapabilities (strmif.h)
description: The CheckCapabilities method queries whether a stream has specified seeking capabilities.
helpviewer_keywords: ["CheckCapabilities","CheckCapabilities method [DirectShow]","CheckCapabilities method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","CheckCapabilities method","IMediaSeeking.CheckCapabilities","IMediaSeeking::CheckCapabilities","IMediaSeekingCheckCapabilities","dshow.imediaseeking_checkcapabilities","strmif/IMediaSeeking::CheckCapabilities"]
old-location: dshow\imediaseeking_checkcapabilities.htm
tech.root: dshow
ms.assetid: d0062f66-213d-4f91-9f73-780be39ee432
ms.date: 4/26/2023
ms.keywords: CheckCapabilities, CheckCapabilities method [DirectShow], CheckCapabilities method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],CheckCapabilities method, IMediaSeeking.CheckCapabilities, IMediaSeeking::CheckCapabilities, IMediaSeekingCheckCapabilities, dshow.imediaseeking_checkcapabilities, strmif/IMediaSeeking::CheckCapabilities
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
 - IMediaSeeking::CheckCapabilities
 - strmif/IMediaSeeking::CheckCapabilities
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
 - IMediaSeeking.CheckCapabilities
---

# IMediaSeeking::CheckCapabilities


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CheckCapabilities</b> method queries whether a stream has specified seeking capabilities.

## -parameters

### -param pCapabilities [in, out]

On input, a pointer to a variable that contains a bitwise <b>OR</b> of one or more <a href="/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities">AM_SEEKING_SEEKING_CAPABILITIES</a> attributes. When the method returns, the value indicates which of those attributes are available.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Some but not all of the capabilities in <i>pCapabilities</i> are present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
All capabilities in <i>pCapabilities</i> are present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No capabilities in <i>pCapabilities</i> are present.

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

If you are only interested in a few specific capabilities, calling this method is more efficient than calling <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcapabilities">IMediaSeeking::GetCapabilities</a>, which checks all the stream's seeking capabilities.

To call this method, declare a <b>DWORD</b> variable and set the value to the bitwise-<b>OR</b> combination of the <a href="/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities">AM_SEEKING_SEEKING_CAPABILITIES</a> flags that you want to test. Pass the address of this value in the <i>pCapabilities</i> parameter. When the method returns, <i>pCapabilities</i> contains a subset of the original bits, indicating which capabilities are present. The return value indicates whether some, none, or all of the requested capabilities are present.

The following code example shows how to find out whether the stream supports forward seeking, backward seeking, and absolute seeking.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Set flags for the capabilities you want to check.

DWORD dwCaps = AM_SEEKING_CanSeekAbsolute | 
               AM_SEEKING_CanSeekForwards |
               AM_SEEKING_CanSeekBackwards;

HRESULT hr = pMediaSeeking-&gt;CheckCapabilities(&amp;dwCaps);
if(FAILED(hr)) 
{
    // The stream cannot seek.
}
else if (hr == S_OK) 
{   
    // The stream can seek forward, backward, and to an absolute position.
}
else if (hr == S_FALSE) // The stream has some of the capabilities.
{
    if (dwCaps &amp; AM_SEEKING_CanSeekAbsolute)
    {
        // The stream can seek to an absolute position.
    }
    if (dwCaps &amp; AM_SEEKING_CanSeekForwards)
    {
        // The stream can seek forward.
    }
    if (dwCaps &amp; AM_SEEKING_CanSeekBackwards)
    {
        // The stream can seek backward.
    }
}
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>

