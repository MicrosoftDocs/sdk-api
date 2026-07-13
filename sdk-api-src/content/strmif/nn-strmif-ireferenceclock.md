---
UID: NN:strmif.IReferenceClock
title: IReferenceClock (strmif.h)
description: The IReferenceClock interface provides the reference time for the filter graph.Filters that can act as a reference clock can expose this interface.
helpviewer_keywords: ["IReferenceClock","IReferenceClock interface [DirectShow]","IReferenceClock interface [DirectShow]","described","IReferenceClockInterface","dshow.ireferenceclock","strmif/IReferenceClock"]
old-location: dshow\ireferenceclock.htm
tech.root: dshow
ms.assetid: 9818c67d-dfbe-4498-a744-d2efaa4bfb58
ms.date: 4/26/2023
ms.keywords: IReferenceClock, IReferenceClock interface [DirectShow], IReferenceClock interface [DirectShow],described, IReferenceClockInterface, dshow.ireferenceclock, strmif/IReferenceClock
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
 - IReferenceClock
 - strmif/IReferenceClock
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
 - IReferenceClock
---

# IReferenceClock interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IReferenceClock</code> interface provides the reference time for the filter graph.

Filters that can act as a reference clock can expose this interface. It is also exposed by the <a href="/windows/desktop/DirectShow/system-reference-clock">System Reference Clock</a>. The filter graph manager uses this interface to synchronize the filter graph. Applications can use this interface to retrieve the current reference time, or to request notification of an elapsed time.

For more information, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

<b>Filter developers: </b>Implement this interface if you are writing a filter that generates reliable clock times. For example, audio renderers implement this interface, because audio sound boards usually contain a reference clock. Use the <a href="/windows/desktop/DirectShow/cbasereferenceclock">CBaseReferenceClock</a> class to implement this interface.

To increase the chances that a non-rendering filter will be selected by the Filter Graph Manager as the reference close, follow these steps:

<ol>
<li>Implement <code>IReferenceClock</code> in the filter.</li>
<li>Implement <a href="/windows/desktop/api/strmif/nn-strmif-iamfiltermiscflags">IAMFilterMiscFlags</a> in the filter.</li>
<li>Return AM_FILTER_MISC_FLAGS_IS_SOURCE from <a href="/windows/desktop/api/strmif/nf-strmif-iamfiltermiscflags-getmiscflags">IAMFilterMiscFlags::GetMiscFlags</a>.</li>
<li>Implement <a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource</a> on all output pins.</li>
<li>Return (* pFlags) = 0 from <a href="/windows/desktop/api/strmif/nf-strmif-iampushsource-getpushsourceflags">IAMPushSource::GetPushSourceFlags</a>.</li>
<li>You may return E_NOTIMPL from all other <b>IAMPushSource</b> methods.</li>
</ol>

## -inheritance

The <b>IReferenceClock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceClock</b> also has these types of members:

