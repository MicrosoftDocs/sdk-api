---
UID: NN:strmif.IReferenceClockTimerControl
title: IReferenceClockTimerControl (strmif.h)
author: windows-sdk-content
description: The IReferenceClockTimerControl interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow System Reference Clock.
old-location: dshow\ireferenceclocktimercontrol.htm
tech.root: DirectShow
ms.assetid: 08638917-88b1-42f0-8324-ae6fb9afe5bd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReferenceClockTimerControl, IReferenceClockTimerControl interface [DirectShow], IReferenceClockTimerControl interface [DirectShow],described, IReferenceClockTimerControlInterface, dshow.ireferenceclocktimercontrol, strmif/IReferenceClockTimerControl
ms.topic: interface
f1_keywords: 
 - "strmif/IReferenceClockTimerControl"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceClockTimerControl interface


## -description



The <code>IReferenceClockTimerControl</code> interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow <a href="https://docs.microsoft.com/windows/desktop/DirectShow/system-reference-clock">System Reference Clock</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceClockTimerControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceClockTimerControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceClockTimerControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution">GetDefaultTimerResolution</a>
</td>
<td align="left" width="63%">
Returns the timer resolution that was requested by the reference clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution">SetDefaultTimerResolution</a>
</td>
<td align="left" width="63%">
Sets the minimum timer resolution.

</td>
</tr>
</table> 


## -remarks



By default, the system reference clock in DirectShow sets the timer period to the minimum value allowed by the timer. Typically, this value is 1 millisecond.

The timer period is a global settings in Windows. A higher resolution can improve the accuracy of time-out intervals in wait functions. However, it can also reduce overall system performance, because the thread scheduler switches tasks more often. High resolutions can also prevent the CPU power management system from entering power-saving modes. Setting a higher resolution does not improve the accuracy of the high-resolution performance counter.

The main purpose of this interface is to override the reference clock's default timer setting. To do so, call <b>SetDefaultTimerResolution</b> with the value zero. This can result in a lower timer resolution, which might enable the user's computer to enter a power saving mode. (The actual behavior depends on many other factors, such as what other processes are running.) The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter uses this interface as described here.

If a DirectShow filter requires a higher timer resolution, it should call <a href="https://docs.microsoft.com/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod">timeBeginPeriod</a>. Typically this requirement would apply only to renderer filters.



