---
UID: NN:tapi3cc.ITQueue
title: ITQueue (tapi3cc.h)
author: windows-sdk-content
description: Gets and sets information concerning a queue. The IEnumQueue::Next and ITACDGroup::get_Queues methods create the ITQueue interface.
old-location: tapi3\itqueue.htm
tech.root: Tapi
ms.assetid: dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# ITQueue interface


## -description


Gets and sets information concerning a queue. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumqueue-next">IEnumQueue::Next</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-get_queues">ITACDGroup::get_Queues</a> methods create the 
<b>ITQueue</b> interface.

See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITQueue</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITQueue</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_averagewaittime">get_AverageWaitTime</a>
</td>
<td align="left" width="63%">
Gets average wait time (in seconds) for a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_currentcallsqueued">get_CurrentCallsQueued</a>
</td>
<td align="left" width="63%">
Gets number of incoming calls in queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_currentlongestwaittime">get_CurrentLongestWaitTime</a>
</td>
<td align="left" width="63%">
Gets longest time a currently waiting call has been in queue (in seconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_finaldisposition">get_FinalDisposition</a>
</td>
<td align="left" width="63%">
Gets total calls reaching the bottom of a call guide. Indicates a problem with queue design or response times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_longesteverwaittime">get_LongestEverWaitTime</a>
</td>
<td align="left" width="63%">
Gets longest time any call waited in queue (in seconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_measurementperiod">get_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Gets period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets queue name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_totalcallsabandoned">get_TotalCallsAdandoned</a>
</td>
<td align="left" width="63%">
Gets number of abandoned calls during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_totalcallsflowedin">get_TotalCallsFlowedIn</a>
</td>
<td align="left" width="63%">
Gets total calls that flowed into this queue (passed down from another queue or ACD group) during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_totalcallsflowedout">get_TotalCallsFlowedOut</a>
</td>
<td align="left" width="63%">
Gets total calls that flowed out this queue (passed down to another queue or ACD group) during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-get_totalcallsqueued">get_TotalCallsQueued</a>
</td>
<td align="left" width="63%">
Gets total incoming calls for this queue during this measurement period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueue-put_measurementperiod">put_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Sets period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
</table> 

