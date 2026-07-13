---
UID: NF:strmif.IReferenceClock.AdviseTime
title: IReferenceClock::AdviseTime (strmif.h)
description: The AdviseTime method creates a one-shot advise request.
helpviewer_keywords: ["AdviseTime","AdviseTime method [DirectShow]","AdviseTime method [DirectShow]","IReferenceClock interface","IReferenceClock interface [DirectShow]","AdviseTime method","IReferenceClock.AdviseTime","IReferenceClock::AdviseTime","IReferenceClockAdviseTime","dshow.ireferenceclock_advisetime","strmif/IReferenceClock::AdviseTime"]
old-location: dshow\ireferenceclock_advisetime.htm
tech.root: dshow
ms.assetid: 22f0c987-a3ae-4d6e-9184-a0a4282340aa
ms.date: 4/26/2023
ms.keywords: AdviseTime, AdviseTime method [DirectShow], AdviseTime method [DirectShow],IReferenceClock interface, IReferenceClock interface [DirectShow],AdviseTime method, IReferenceClock.AdviseTime, IReferenceClock::AdviseTime, IReferenceClockAdviseTime, dshow.ireferenceclock_advisetime, strmif/IReferenceClock::AdviseTime
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
 - IReferenceClock::AdviseTime
 - strmif/IReferenceClock::AdviseTime
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
 - IReferenceClock.AdviseTime
---

# IReferenceClock::AdviseTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AdviseTime</code> method creates a one-shot advise request.

## -parameters

### -param baseTime [in]

Base reference time, in 100-nanosecond units. See Remarks.

### -param streamTime [in]

Stream offset time, in 100-nanosecond units. See Remarks.

### -param hEvent [in]

Handle to an event, created by the caller.

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

This method creates a one-shot advise request for the reference time <i>rtBaseTime</i> + <i>rtStreamTime</i>. The sum must be greater than zero and less than MAX_TIME, or the method returns E_INVALIDARG. At the requested time, the clock signals the event specified in the <i>hEvent</i> parameter.

To cancel the notification before the time is reached, call the <a href="/windows/desktop/api/strmif/nf-strmif-ireferenceclock-unadvise">Unadvise</a> method and pass the <i>pdwAdviseToken</i> value returned from this call. After the notification has occurred, the clock automatically clears it, so it is not necessary to call <b>Unadvise</b>. However, it is not an error to do so.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock Interface</a>