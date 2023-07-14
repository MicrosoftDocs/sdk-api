---
UID: NN:tuner.IESEventService
title: IESEventService (tuner.h)
description: Implements an event service that includes methods that raise events derived from the IESEvent interface.
helpviewer_keywords: ["IESEventService","IESEventService interface [Microsoft TV Technologies]","IESEventService interface [Microsoft TV Technologies]","described","mstv.ieseventservice","tuner/IESEventService"]
old-location: mstv\ieseventservice.htm
tech.root: mstv
ms.assetid: 2720d616-18a6-488e-98ef-565768c22c2a
ms.date: 12/05/2018
ms.keywords: IESEventService, IESEventService interface [Microsoft TV Technologies], IESEventService interface [Microsoft TV Technologies],described, mstv.ieseventservice, tuner/IESEventService
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESEventService
 - tuner/IESEventService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEventService
---

# IESEventService interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements an event service that includes methods that raise events derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. Media Transform Devices in a Protected Broadcast Driver Architecture (PBDA) graph can use this interface to send specific types of these events to Media Sink Devices that have registered to receive them. The <b>IESEventService</b> interface is an outgoing connection point interface.

## -inheritance

The <b>IESEventService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEventService</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEventService)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>
