---
UID: NF:strmif.IReferenceClock.AdvisePeriodic
title: IReferenceClock::AdvisePeriodic (strmif.h)
description: The AdvisePeriodic method creates a periodic advise request.
helpviewer_keywords: ["AdvisePeriodic","AdvisePeriodic method [DirectShow]","AdvisePeriodic method [DirectShow]","IReferenceClock interface","IReferenceClock interface [DirectShow]","AdvisePeriodic method","IReferenceClock.AdvisePeriodic","IReferenceClock::AdvisePeriodic","IReferenceClockAdvisePeriodic","dshow.ireferenceclock_adviseperiodic","strmif/IReferenceClock::AdvisePeriodic"]
old-location: dshow\ireferenceclock_adviseperiodic.htm
tech.root: dshow
ms.assetid: c8e2545b-ea3c-441c-8721-e7dec09d100e
ms.date: 4/26/2023
ms.keywords: AdvisePeriodic, AdvisePeriodic method [DirectShow], AdvisePeriodic method [DirectShow],IReferenceClock interface, IReferenceClock interface [DirectShow],AdvisePeriodic method, IReferenceClock.AdvisePeriodic, IReferenceClock::AdvisePeriodic, IReferenceClockAdvisePeriodic, dshow.ireferenceclock_adviseperiodic, strmif/IReferenceClock::AdvisePeriodic
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
 - IReferenceClock::AdvisePeriodic
 - strmif/IReferenceClock::AdvisePeriodic
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
 - IReferenceClock.AdvisePeriodic
---

# IReferenceClock::AdvisePeriodic


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AdvisePeriodic</code> method creates a periodic advise request.

## -parameters

### -param startTime [in]

Time of the first notification, in 100-nanosecond units. Must be greater than zero and less than MAX_TIME.

### -param periodTime [in]

Time between notifications, in 100-nanosecond units. Must be greater than zero.

### -param hSemaphore [in]

Handle to a semaphore, created by the caller.

### -param pdwAdviseCookie [out]

Pointer to a variable that receives an identifier for the advise request.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid time values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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

At each notification time, the clock releases the semaphore specified in the <i>hSemaphore</i> parameter. When no further notifications are required, call <a href="/windows/desktop/api/strmif/nf-strmif-ireferenceclock-unadvise">IReferenceClock::Unadvise</a> and pass the <i>pdwAdviseToken</i> value returned from this call.

The following code example creates an advise request that signals five seconds from the time it is created, and again every second thereafter:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IReferenceClock *pRefClock = NULL;
// Get an IReferenceClock pointer (not shown).

DWORD          dwAdviseToken;
HANDLE         hSemaphore = CreateSemaphore(NULL, 0, 0x7FFFFFFF, NULL);
REFERENCE_TIME rtPeriodTime = 10000000; // A one-second interval
REFERENCE_TIME rtNow;

pRefClock-&gt;GetTime(&amp;rtNow);
pRefClock-&gt;AdvisePeriodic(rtNow + (5 * rtPeriodTime),
                          rtPeriodTime, 
                          hSemaphore, 
                          &amp;dwAdviseToken);
...

pRefClock-&gt;Unadvise(dwAdviseToken);
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock Interface</a>