---
UID: NN:tuner.IESRequestTunerEvent
title: IESRequestTunerEvent (tuner.h)
author: windows-sdk-content
description: Contains methods that enable a Protected Broadcast Driver Architecture (PBDA)-supported device to get exclusive access to a tuner and its Conditional Access Services (CAS).
old-location: mstv\iesrequesttunerevent.htm
tech.root: mstv
ms.assetid: da1183a3-6f31-402a-b103-448cf13705a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESRequestTunerEvent, IESRequestTunerEvent interface [Microsoft TV Technologies], IESRequestTunerEvent interface [Microsoft TV Technologies],described, mstv.iesrequesttunerevent, tuner/IESRequestTunerEvent
ms.topic: interface
f1_keywords: 
 - "tuner/IESRequestTunerEvent"
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESRequestTunerEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESRequestTunerEvent interface


## -description


Contains methods that enable a Protected Broadcast Driver Architecture (PBDA)-supported device  to get exclusive access to a tuner and its Conditional Access Services (CAS).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESRequestTunerEvent</b> interface inherits from <b>IESEvent</b>. <b>IESRequestTunerEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESRequestTunerEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesrequesttunerevent-getconsequences">GetConsequences</a>
</td>
<td align="left" width="63%">
Gets a code that indicates consquences of a device request for exclusive access to a tuner and its CAS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesrequesttunerevent-getestimatedtime">GetEstimatedTime</a>
</td>
<td align="left" width="63%">
Gets the amount of time a device estimates it  needs exclusive access to a tuner and its CAS.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesrequesttunerevent-getpriority">GetPriority</a>
</td>
<td align="left" width="63%">
Gets a code that indicates the the priority of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesrequesttunerevent-getreason">GetReason</a>
</td>
<td align="left" width="63%">
Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its CAS.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESRequestTunerEvent)</code>.



