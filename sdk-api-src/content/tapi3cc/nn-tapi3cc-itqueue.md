---
UID: NN:tapi3cc.ITQueue
title: ITQueue
author: windows-sdk-content
description: Gets and sets information concerning a queue. The IEnumQueue::Next and ITACDGroup::get_Queues methods create the ITQueue interface.
old-location: tapi3\itqueue.htm
tech.root: Tapi
ms.assetid: dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITQueue, ITQueue interface [TAPI 2.2], ITQueue interface [TAPI 2.2],described, _tapi3_itqueue, tapi3.itqueue, tapi3cc/ITQueue
ms.topic: interface
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITQueue interface


## -description


Gets and sets information concerning a queue. The 
<a href="https://msdn.microsoft.com/95c1a919-4138-49c1-ad3a-2b15d928e84f">IEnumQueue::Next</a> and 
<a href="https://msdn.microsoft.com/f285fea5-4c08-4d30-8378-0b0aeeea8226">ITACDGroup::get_Queues</a> methods create the 
<b>ITQueue</b> interface.

See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94883656-8a72-464d-9478-89f698c98db8">get_AverageWaitTime</a>
</td>
<td align="left" width="63%">
Gets average wait time (in seconds) for a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbc6e38c-c4e9-45ea-8c9a-9bb8116c1e2f">get_CurrentCallsQueued</a>
</td>
<td align="left" width="63%">
Gets number of incoming calls in queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3334932-2029-4e10-a12c-605697a2bb36">get_CurrentLongestWaitTime</a>
</td>
<td align="left" width="63%">
Gets longest time a currently waiting call has been in queue (in seconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/024680d2-5b27-4002-a492-54b35a2d3513">get_FinalDisposition</a>
</td>
<td align="left" width="63%">
Gets total calls reaching the bottom of a call guide. Indicates a problem with queue design or response times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/686ea264-a826-4205-a422-7d1dc3d430f8">get_LongestEverWaitTime</a>
</td>
<td align="left" width="63%">
Gets longest time any call waited in queue (in seconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/931fb7dd-8c9b-4b1e-9296-6335e5a7e164">get_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Gets period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2a9f402-9341-426f-8994-902b754ceed9">get_Name</a>
</td>
<td align="left" width="63%">
Gets queue name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db1309e-f6df-47f8-a695-7bf05d360d99">get_TotalCallsAdandoned</a>
</td>
<td align="left" width="63%">
Gets number of abandoned calls during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c351937-0f26-478a-a475-37bb67aa61b9">get_TotalCallsFlowedIn</a>
</td>
<td align="left" width="63%">
Gets total calls that flowed into this queue (passed down from another queue or ACD group) during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e12cc43b-54d9-4e65-82e8-a2e819ea219e">get_TotalCallsFlowedOut</a>
</td>
<td align="left" width="63%">
Gets total calls that flowed out this queue (passed down to another queue or ACD group) during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45a1a47a-4cbe-47dd-ad48-218e74fe74b4">get_TotalCallsQueued</a>
</td>
<td align="left" width="63%">
Gets total incoming calls for this queue during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e32b2ae-c4e5-4624-b970-673c950dee3b">put_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Sets period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
</table> 

