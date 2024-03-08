---
UID: NN:tuner.IESEvents
title: IESEvents (tuner.h)
description: Implements event handling for devices that have registered to receive specific events derived from the IESEvent interface. In a Protected Broadcast Driver Architecture graph, Media Sink Devices implement this interface to register for events.
helpviewer_keywords: ["IESEvents","IESEvents interface [Microsoft TV Technologies]","IESEvents interface [Microsoft TV Technologies]","described","mstv.iesevents","tuner/IESEvents"]
old-location: mstv\iesevents.htm
tech.root: mstv
ms.assetid: 1921f632-bb3b-4833-aa25-9caa3d65363f
ms.date: 12/05/2018
ms.keywords: IESEvents, IESEvents interface [Microsoft TV Technologies], IESEvents interface [Microsoft TV Technologies],described, mstv.iesevents, tuner/IESEvents
f1_keywords:
- tuner/IESEvents
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
- IESEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvents interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Implements event handling for devices that have registered to receive specific events derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. In a Protected Broadcast Driver Architecture graph, Media Sink Devices implement this interface to register for events.
      


## -inheritance

The <b>IESEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEvents</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -members

The <b>IESEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevents-oneseventreceived">OnESEventReceived</a>
</td>
<td align="left" width="63%">
Defines a handler for events derived from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEvents)</code>.