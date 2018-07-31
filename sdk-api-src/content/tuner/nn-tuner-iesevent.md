---
UID: NN:tuner.IESEvent
title: IESEvent
author: windows-sdk-content
description: Implements a generic event interface that can deliver and encapsulate events that are raised by devices that work with the Protected Broadcast Driver Interface (PBDA).
old-location: mstv\iesevent.htm
old-project: mstv
ms.assetid: 3c375480-c6df-4bb0-b417-5765b0bed9bf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IESEvent, IESEvent interface [Microsoft TV Technologies], IESEvent interface [Microsoft TV Technologies],described, mstv.iesevent, tuner/IESEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvent interface


## -description


Implements a generic event interface that can deliver and encapsulate events that are raised by devices that work with the Protected Broadcast Driver Interface (PBDA). PBDA devices pass <b>IESEvent</b> objects in calls to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.
      Any devices that have registered to receive an event can call <b>IESEvent</b> methods to get data from the event.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IESEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
</td>
<td align="left" width="63%">
Returns a byte array that contains the event data.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a7d62de-71fc-40fa-9944-d41e33243cc5">GetEventId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for the event.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8418116a-2393-4a1b-8c5b-2356d373e426">GetEventType</a>
</td>
<td align="left" width="63%">
Gets the GUID that identifies the event type.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a1c98af-a753-40e5-bea8-825863f94172">GetStringData</a>
</td>
<td align="left" width="63%">
Gets the event data in Unicode string format.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e8d5a94-6fa1-453b-bbd4-396d60bb2aa0">SetCompletionStatus</a>
</td>
<td align="left" width="63%">
Sets the event completion status for clients that  process the event.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">FireESEvent</a>



<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEvents</a>
 

 

