---
UID: NN:strmif.IReferenceClockTimerControl
title: IReferenceClockTimerControl
author: windows-sdk-content
description: The IReferenceClockTimerControl interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow System Reference Clock.
old-location: dshow\ireferenceclocktimercontrol.htm
tech.root: DirectShow
ms.assetid: 08638917-88b1-42f0-8324-ae6fb9afe5bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IReferenceClockTimerControl, IReferenceClockTimerControl interface [DirectShow], IReferenceClockTimerControl interface [DirectShow],described, IReferenceClockTimerControlInterface, dshow.ireferenceclocktimercontrol, strmif/IReferenceClockTimerControl
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceClockTimerControl interface


## -description



The <code>IReferenceClockTimerControl</code> interface changes the timer period used by a reference clock. This interface is exposed by the DirectShow <a href="https://msdn.microsoft.com/0247dcb9-64ee-4562-944a-44bcfae80f2d">System Reference Clock</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceClockTimerControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceClockTimerControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8382bc39-bc3d-43a1-aa06-16a4eecbdc7a">GetDefaultTimerResolution</a>
</td>
<td align="left" width="63%">
Returns the timer resolution that was requested by the reference clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d13d14a7-39dd-4281-9926-4af97cc5d450">SetDefaultTimerResolution</a>
</td>
<td align="left" width="63%">
Sets the minimum timer resolution.

</td>
</tr>
</table> 


## -remarks



By default, the system reference clock in DirectShow sets the timer period to the minimum value allowed by the timer. Typically, this value is 1 millisecond.

The timer period is a global settings in Windows. A higher resolution can improve the accuracy of time-out intervals in wait functions. However, it can also reduce overall system performance, because the thread scheduler switches tasks more often. High resolutions can also prevent the CPU power management system from entering power-saving modes. Setting a higher resolution does not improve the accuracy of the high-resolution performance counter.

The main purpose of this interface is to override the reference clock's default timer setting. To do so, call <b>SetDefaultTimerResolution</b> with the value zero. This can result in a lower timer resolution, which might enable the user's computer to enter a power saving mode. (The actual behavior depends on many other factors, such as what other processes are running.) The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter uses this interface as described here.

If a DirectShow filter requires a higher timer resolution, it should call <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a>. Typically this requirement would apply only to renderer filters.



