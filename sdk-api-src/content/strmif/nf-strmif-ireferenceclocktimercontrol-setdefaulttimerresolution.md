---
UID: NF:strmif.IReferenceClockTimerControl.SetDefaultTimerResolution
title: IReferenceClockTimerControl::SetDefaultTimerResolution (strmif.h)
description: The SetDefaultTimerResolution method sets the minimum timer resolution.
helpviewer_keywords: ["IReferenceClockTimerControl interface [DirectShow]","SetDefaultTimerResolution method","IReferenceClockTimerControl.SetDefaultTimerResolution","IReferenceClockTimerControl::SetDefaultTimerResolution","IReferenceClockTimerControlSetDefaultTimerResoluti","SetDefaultTimerResolution","SetDefaultTimerResolution method [DirectShow]","SetDefaultTimerResolution method [DirectShow]","IReferenceClockTimerControl interface","dshow.ireferenceclocktimercontrol_setdefaulttimerresolution","strmif/IReferenceClockTimerControl::SetDefaultTimerResolution"]
old-location: dshow\ireferenceclocktimercontrol_setdefaulttimerresolution.htm
tech.root: dshow
ms.assetid: d13d14a7-39dd-4281-9926-4af97cc5d450
ms.date: 4/26/2023
ms.keywords: IReferenceClockTimerControl interface [DirectShow],SetDefaultTimerResolution method, IReferenceClockTimerControl.SetDefaultTimerResolution, IReferenceClockTimerControl::SetDefaultTimerResolution, IReferenceClockTimerControlSetDefaultTimerResoluti, SetDefaultTimerResolution, SetDefaultTimerResolution method [DirectShow], SetDefaultTimerResolution method [DirectShow],IReferenceClockTimerControl interface, dshow.ireferenceclocktimercontrol_setdefaulttimerresolution, strmif/IReferenceClockTimerControl::SetDefaultTimerResolution
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
 - IReferenceClockTimerControl::SetDefaultTimerResolution
 - strmif/IReferenceClockTimerControl::SetDefaultTimerResolution
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
 - IReferenceClockTimerControl.SetDefaultTimerResolution
---

# IReferenceClockTimerControl::SetDefaultTimerResolution


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDefaultTimerResolution</code> method sets the minimum timer resolution.

## -parameters

### -param timerResolution [in]

Minimum timer resolution, in 100-nanosecond units. If the value is zero, the reference clock cancels its previous request.

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
</table>

## -remarks

The reference clock attempts to set the period of the timer to <i>timerResolution</i>. The actual period of the timer might differ, depending on the hardware. To find the minimum and maximum timer resolution, call the <a href="/windows/desktop/api/timeapi/nf-timeapi-timegetdevcaps">timeGetDevCaps</a> function. The reference clock sets the timer resolution is set by calling <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a>. If <i>timerResolution</i> is 0, the method cancels the previous timer request by calling <a href="/windows/desktop/api/timeapi/nf-timeapi-timeendperiod">timeEndPeriod</a>. (When the reference clock is destroyed, it automatically cancels any previous request.)

If this method is not called, the reference clock sets the timer resolution to 1 millisecond. To get the best power management performance, it is recommended that you call this method with the value zero. This overrides the clock's default setting of 1 millisecond. If any filters in the graph require a higher timer resolution, they can call <a href="/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a> individually. Typically only renderers should require a particular timer resolution.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclocktimercontrol">IReferenceClockTimerControl Interface</a>