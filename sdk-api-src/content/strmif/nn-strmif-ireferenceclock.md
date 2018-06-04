---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IReferenceClock interface


## -description



The <code>IReferenceClock</code> interface provides the reference time for the filter graph.

Filters that can act as a reference clock can expose this interface. It is also exposed by the <a href="https://msdn.microsoft.com/0247dcb9-64ee-4562-944a-44bcfae80f2d">System Reference Clock</a>. The filter graph manager uses this interface to synchronize the filter graph. Applications can use this interface to retrieve the current reference time, or to request notification of an elapsed time.

For more information, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.

<b>Filter developers: </b>Implement this interface if you are writing a filter that generates reliable clock times. For example, audio renderers implement this interface, because audio sound boards usually contain a reference clock. Use the <a href="https://msdn.microsoft.com/898e1968-a9ab-4bb9-abf0-943bfae502e2">CBaseReferenceClock</a> class to implement this interface.

To increase the chances that a non-rendering filter will be selected by the Filter Graph Manager as the reference close, follow these steps:

<ol>
<li>Implement <code>IReferenceClock</code> in the filter.</li>
<li>Implement <a href="https://msdn.microsoft.com/f9f3eaf9-4afa-412f-aa8f-b75e787cfecb">IAMFilterMiscFlags</a> in the filter.</li>
<li>Return AM_FILTER_MISC_FLAGS_IS_SOURCE from <a href="https://msdn.microsoft.com/03728d28-a3e5-4ac5-b637-1daa173e5e88">IAMFilterMiscFlags::GetMiscFlags</a>.</li>
<li>Implement <a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource</a> on all output pins.</li>
<li>Return (* pFlags) = 0 from <a href="https://msdn.microsoft.com/3e72367f-a066-43ad-9f96-648cad13b43d">IAMPushSource::GetPushSourceFlags</a>.</li>
<li>You may return E_NOTIMPL from all other <b>IAMPushSource</b> methods.</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceClock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceClock</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c8e2545b-ea3c-441c-8721-e7dec09d100e">AdvisePeriodic</a>
</td>
<td align="left" width="63%">
Creates a periodic advise request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f0c987-a3ae-4d6e-9184-a0a4282340aa">AdviseTime</a>
</td>
<td align="left" width="63%">
Creates a one-shot advise request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fcf8b8a-f449-4f42-8061-cc4116867d9d">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the current reference time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f032036-4502-473a-93e1-976a66d8bde1">Unadvise</a>
</td>
<td align="left" width="63%">
Removes a pending advise request.

</td>
</tr>
</table> 

