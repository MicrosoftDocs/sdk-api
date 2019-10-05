---
UID: NN:bdatif.IGuideDataEvent
title: IGuideDataEvent (bdatif.h)
author: windows-sdk-content
description: The IGuideDataEvent interface is used to receive events from the BDA MPEG-2 Transport Information Filter (TIF).This interface is an outgoing connection-point interface.
old-location: mstv\iguidedataevent.htm
tech.root: mstv
ms.assetid: 9da565f2-fbcb-4d71-ae40-7d9821f46630
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGuideDataEvent, IGuideDataEvent interface [Microsoft TV Technologies], IGuideDataEvent interface [Microsoft TV Technologies],described, IGuideDataEventInterface, bdatif/IGuideDataEvent, mstv.iguidedataevent
ms.topic: interface
f1_keywords: 
 - "bdatif/IGuideDataEvent"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGuideDataEvent interface


## -description



The <b>IGuideDataEvent</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF).

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection. The event sink must not block the calling thread. If the client requires additional information about the event, it should make calls on a separate thread.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGuideDataEvent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGuideDataEvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-guidedataacquired">GuideDataAcquired</a>
</td>
<td align="left" width="63%">
Called when a complete set of guide data has been acquired from the current transport stream. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-programchanged">ProgramChanged</a>
</td>
<td align="left" width="63%">
Called when information about one or more programs has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-programdeleted">ProgramDeleted</a>
</td>
<td align="left" width="63%">
Called when a program has been deleted. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-scheduledeleted">ScheduleDeleted</a>
</td>
<td align="left" width="63%">
Called when a schedule entry has been deleted. (Currently not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-scheduleentrychanged">ScheduleEntryChanged</a>
</td>
<td align="left" width="63%">
Called when information about one or more schedule entries has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-servicechanged">ServiceChanged</a>
</td>
<td align="left" width="63%">
Called when a service has been changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-servicedeleted">ServiceDeleted</a>
</td>
<td align="left" width="63%">
Called when a service has been deleted. (Currently not supported.)

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideDataEvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

