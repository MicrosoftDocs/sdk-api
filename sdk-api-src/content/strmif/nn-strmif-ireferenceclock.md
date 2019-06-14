---
UID: NN:strmif.IReferenceClock
title: IReferenceClock (strmif.h)
author: windows-sdk-content
description: The IReferenceClock interface provides the reference time for the filter graph.Filters that can act as a reference clock can expose this interface.
old-location: dshow\ireferenceclock.htm
tech.root: DirectShow
ms.assetid: 9818c67d-dfbe-4498-a744-d2efaa4bfb58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReferenceClock, IReferenceClock interface [DirectShow], IReferenceClock interface [DirectShow],described, IReferenceClockInterface, dshow.ireferenceclock, strmif/IReferenceClock
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceClock interface


## -description



The <code>IReferenceClock</code> interface provides the reference time for the filter graph.

Filters that can act as a reference clock can expose this interface. It is also exposed by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/system-reference-clock">System Reference Clock</a>. The filter graph manager uses this interface to synchronize the filter graph. Applications can use this interface to retrieve the current reference time, or to request notification of an elapsed time.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

<b>Filter developers: </b>Implement this interface if you are writing a filter that generates reliable clock times. For example, audio renderers implement this interface, because audio sound boards usually contain a reference clock. Use the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasereferenceclock">CBaseReferenceClock</a> class to implement this interface.

To increase the chances that a non-rendering filter will be selected by the Filter Graph Manager as the reference close, follow these steps:

<ol>
<li>Implement <code>IReferenceClock</code> in the filter.</li>
<li>Implement <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamfiltermiscflags">IAMFilterMiscFlags</a> in the filter.</li>
<li>Return AM_FILTER_MISC_FLAGS_IS_SOURCE from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamfiltermiscflags-getmiscflags">IAMFilterMiscFlags::GetMiscFlags</a>.</li>
<li>Implement <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource</a> on all output pins.</li>
<li>Return (* pFlags) = 0 from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iampushsource-getpushsourceflags">IAMPushSource::GetPushSourceFlags</a>.</li>
<li>You may return E_NOTIMPL from all other <b>IAMPushSource</b> methods.</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceClock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclock-adviseperiodic">AdvisePeriodic</a>
</td>
<td align="left" width="63%">
Creates a periodic advise request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclock-advisetime">AdviseTime</a>
</td>
<td align="left" width="63%">
Creates a one-shot advise request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclock-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current reference time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ireferenceclock-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Removes a pending advise request.

</td>
</tr>
</table> 

