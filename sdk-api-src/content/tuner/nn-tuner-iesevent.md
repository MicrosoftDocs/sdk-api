---
UID: NN:tuner.IESEvent
title: IESEvent (tuner.h)
description: Implements a generic event interface that can deliver and encapsulate events that are raised by devices that work with the Protected Broadcast Driver Interface (PBDA).
helpviewer_keywords: ["IESEvent","IESEvent interface [Microsoft TV Technologies]","IESEvent interface [Microsoft TV Technologies]","described","mstv.iesevent","tuner/IESEvent"]
old-location: mstv\iesevent.htm
tech.root: mstv
ms.assetid: 3c375480-c6df-4bb0-b417-5765b0bed9bf
ms.date: 12/05/2018
ms.keywords: IESEvent, IESEvent interface [Microsoft TV Technologies], IESEvent interface [Microsoft TV Technologies],described, mstv.iesevent, tuner/IESEvent
f1_keywords:
- tuner/IESEvent
dev_langs:
- c++
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
- IESEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Implements a generic event interface that can deliver and encapsulate events that are raised by devices that work with the Protected Broadcast Driver Interface (PBDA). PBDA devices pass <b>IESEvent</b> objects in calls to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>.
      Any devices that have registered to receive an event can call <b>IESEvent</b> methods to get data from the event.


## -inheritance

The <b>IESEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -members

The <b>IESEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-getdata">GetData</a>
</td>
<td align="left" width="63%">
Returns a byte array that contains the event data.
          

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-geteventid">GetEventId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for the event.
          

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-geteventtype">GetEventType</a>
</td>
<td align="left" width="63%">
Gets the GUID that identifies the event type.
          

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-getstringdata">GetStringData</a>
</td>
<td align="left" width="63%">
Gets the event data in Unicode string format.
          

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-setcompletionstatus">SetCompletionStatus</a>
</td>
<td align="left" width="63%">
Sets the event completion status for clients that  process the event.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEvent)</code>.




## -see-also




<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">FireESEvent</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEvents</a>
 

 