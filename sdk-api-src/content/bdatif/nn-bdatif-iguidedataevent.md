---
UID: NN:bdatif.IGuideDataEvent
title: IGuideDataEvent
author: windows-sdk-content
description: The IGuideDataEvent interface is used to receive events from the BDA MPEG-2 Transport Information Filter (TIF).This interface is an outgoing connection-point interface.
old-location: mstv\iguidedataevent.htm
tech.root: MSTV
ms.assetid: 9da565f2-fbcb-4d71-ae40-7d9821f46630
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGuideDataEvent, IGuideDataEvent interface [Microsoft TV Technologies], IGuideDataEvent interface [Microsoft TV Technologies],described, IGuideDataEventInterface, bdatif/IGuideDataEvent, mstv.iguidedataevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdatif.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IGuideDataEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent interface


## -description



The <b>IGuideDataEvent</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> (TIF).

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection. The event sink must not block the calling thread. If the client requires additional information about the event, it should make calls on a separate thread.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGuideDataEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGuideDataEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGuideDataEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00f1aec7-4d26-4323-9d7e-c75d9a0c374c">GuideDataAcquired</a>
</td>
<td align="left" width="63%">
Called when a complete set of guide data has been acquired from the current transport stream. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06fcf24b-5d35-4689-9c88-240fe18a46de">ProgramChanged</a>
</td>
<td align="left" width="63%">
Called when information about one or more programs has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a71e139-1c09-473c-8195-0a55601d2f17">ProgramDeleted</a>
</td>
<td align="left" width="63%">
Called when a program has been deleted. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/302c068e-4fab-4045-be9b-664902afd44c">ScheduleDeleted</a>
</td>
<td align="left" width="63%">
Called when a schedule entry has been deleted. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c278a0-8a92-4801-9463-696beb22819e">ScheduleEntryChanged</a>
</td>
<td align="left" width="63%">
Called when information about one or more schedule entries has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75387dd8-e0e2-4fae-8c4a-a0b7b06f61b1">ServiceChanged</a>
</td>
<td align="left" width="63%">
Called when a service has been changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bba15ebe-d1c5-4c71-b052-6b75a7825613">ServiceDeleted</a>
</td>
<td align="left" width="63%">
Called when a service has been deleted. (Currently not supported.)

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideDataEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

