---
UID: NN:strmif.IReferenceClockTimerControl
title: IReferenceClockTimerControl (strmif.h)
description: The IReferenceClockTimerControl interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow System Reference Clock.
helpviewer_keywords: ["IReferenceClockTimerControl","IReferenceClockTimerControl interface [DirectShow]","IReferenceClockTimerControl interface [DirectShow]","described","IReferenceClockTimerControlInterface","dshow.ireferenceclocktimercontrol","strmif/IReferenceClockTimerControl"]
old-location: dshow\ireferenceclocktimercontrol.htm
tech.root: dshow
ms.assetid: 08638917-88b1-42f0-8324-ae6fb9afe5bd
ms.date: 4/26/2023
ms.keywords: IReferenceClockTimerControl, IReferenceClockTimerControl interface [DirectShow], IReferenceClockTimerControl interface [DirectShow],described, IReferenceClockTimerControlInterface, dshow.ireferenceclocktimercontrol, strmif/IReferenceClockTimerControl
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IReferenceClockTimerControl
 - strmif/IReferenceClockTimerControl
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
 - IReferenceClockTimerControl
---

# IReferenceClockTimerControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IReferenceClockTimerControl</code> interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow <a href="/windows/desktop/DirectShow/system-reference-clock">System Reference Clock</a>.

## -inheritance

The <b>IReferenceClockTimerControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceClockTimerControl</b> also has these types of members:

## -remarks

By default, the system reference clock in DirectShow sets the timer period to the minimum value allowed by the timer. Typically, this value is 1 millisecond.

The timer period is a global settings in Windows. A higher resolution can improve the accuracy of time-out intervals in wait functions. However, it can also reduce overall system performance, because the thread scheduler switches tasks more often. High resolutions can also prevent the CPU power management system from entering power-saving modes. Setting a higher resolution does not improve the accuracy of the high-resolution performance counter.

The main purpose of this interface is to override the reference clock's default timer setting. To do so, call <b>SetDefaultTimerResolution</b> with the value zero. This can result in a lower timer resolution, which might enable the user's computer to enter a power saving mode. (The actual behavior depends on many other factors, such as what other processes are running.) The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter uses this interface as described here.

If a DirectShow filter requires a higher timer resolution, it should call <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a>. Typically this requirement would apply only to renderer filters.
