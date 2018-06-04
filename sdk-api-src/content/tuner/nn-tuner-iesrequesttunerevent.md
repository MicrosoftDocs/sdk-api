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

# IESRequestTunerEvent interface


## -description



      Contains methods that enable a Protected Broadcast Driver Architecture (PBDA)-supported device  to get exclusive access to a tuner and its Conditional Access Services (CAS).

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


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
<a href="https://msdn.microsoft.com/39588da7-90e7-4544-b53c-0f0ddb6cd951">GetConsequences</a>
</td>
<td align="left" width="63%">

            Gets a code that indicates consquences of a device request for exclusive access to a tuner and its CAS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9968c1b1-5a4d-45a1-a083-afdbcc616f6d">GetEstimatedTime</a>
</td>
<td align="left" width="63%">

            Gets the amount of time a device estimates it  needs exclusive access to a tuner and its CAS.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0edc656-0628-4020-bf8e-a5cd0bedd7c3">GetPriority</a>
</td>
<td align="left" width="63%">

            Gets a code that indicates the the priority of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8b9080-0299-4ba9-a49d-9ef142e91eb8">GetReason</a>
</td>
<td align="left" width="63%">

            Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its CAS.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESRequestTunerEvent)</code>.



