---
UID: NF:strmif.IReferenceClockTimerControl.GetDefaultTimerResolution
title: IReferenceClockTimerControl::GetDefaultTimerResolution (strmif.h)
description: The GetDefaultTimerResolution method returns the timer resolution that was requested by the reference clock.
helpviewer_keywords: ["GetDefaultTimerResolution","GetDefaultTimerResolution method [DirectShow]","GetDefaultTimerResolution method [DirectShow]","IReferenceClockTimerControl interface","IReferenceClockTimerControl interface [DirectShow]","GetDefaultTimerResolution method","IReferenceClockTimerControl.GetDefaultTimerResolution","IReferenceClockTimerControl::GetDefaultTimerResolution","IReferenceClockTimerControlGetDefaultTimerResoluti","dshow.ireferenceclocktimercontrol_getdefaulttimerresolution","strmif/IReferenceClockTimerControl::GetDefaultTimerResolution"]
old-location: dshow\ireferenceclocktimercontrol_getdefaulttimerresolution.htm
tech.root: dshow
ms.assetid: 8382bc39-bc3d-43a1-aa06-16a4eecbdc7a
ms.date: 4/26/2023
ms.keywords: GetDefaultTimerResolution, GetDefaultTimerResolution method [DirectShow], GetDefaultTimerResolution method [DirectShow],IReferenceClockTimerControl interface, IReferenceClockTimerControl interface [DirectShow],GetDefaultTimerResolution method, IReferenceClockTimerControl.GetDefaultTimerResolution, IReferenceClockTimerControl::GetDefaultTimerResolution, IReferenceClockTimerControlGetDefaultTimerResoluti, dshow.ireferenceclocktimercontrol_getdefaulttimerresolution, strmif/IReferenceClockTimerControl::GetDefaultTimerResolution
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
 - IReferenceClockTimerControl::GetDefaultTimerResolution
 - strmif/IReferenceClockTimerControl::GetDefaultTimerResolution
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
 - IReferenceClockTimerControl.GetDefaultTimerResolution
---

# IReferenceClockTimerControl::GetDefaultTimerResolution


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDefaultTimerResolution</code> method returns the timer resolution that was requested by the reference clock.

## -parameters

### -param pTimerResolution [out]

Receives the requested timer resolution, in 100-nanosecond units.

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

The value returned in <i>pTimerResolution</i> is the period that the reference clock attempts to set on the underlying timer. The actual timer period might differ, depending on the hardware. If the reference clock did not request a minimum timer resolution, the <i>pTimerResolution</i> parameter receives the value zero.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclocktimercontrol">IReferenceClockTimerControl Interface</a>