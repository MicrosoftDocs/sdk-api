---
UID: NN:tuner.IESEventService
title: IESEventService (tuner.h)

description: Implements an event service that includes methods that raise events derived from the IESEvent interface.
old-location: mstv\ieseventservice.htm
tech.root: mstv
ms.assetid: 2720d616-18a6-488e-98ef-565768c22c2a

ms.date: 12/05/2018
ms.keywords: IESEventService, IESEventService interface [Microsoft TV Technologies], IESEventService interface [Microsoft TV Technologies],described, mstv.ieseventservice, tuner/IESEventService
ms.topic: interface
f1_keywords: 
 - "tuner/IESEventService"
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
 - IESEventService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEventService interface


## -description


Implements an event service that includes methods that raise events derived from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. Media Transform Devices in a Protected Broadcast Driver Architecture (PBDA) graph can use this interface to send specific types of these events to Media Sink Devices that have registered to receive them. The <b>IESEventService</b> interface is an outgoing connection point interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESEventService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEventService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESEventService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">FireESEvent</a>
</td>
<td align="left" width="63%">
Raises an event that is derived from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface from a device.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEventService)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>
 

 

