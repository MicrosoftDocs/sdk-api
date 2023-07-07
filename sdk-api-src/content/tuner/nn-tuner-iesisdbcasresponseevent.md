---
UID: NN:tuner.IESIsdbCasResponseEvent
title: IESIsdbCasResponseEvent (tuner.h)
description: Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) IsdbCasResponse event.
helpviewer_keywords: ["IESIsdbCasResponseEvent","IESIsdbCasResponseEvent interface [DirectShow]","IESIsdbCasResponseEvent interface [DirectShow]","described","mstv.iesisdbcasresponseevent","tuner/IESIsdbCasResponseEvent"]
old-location: mstv\iesisdbcasresponseevent.htm
tech.root: mstv
ms.assetid: 141c6798-5dca-495e-bdbe-f07e457a3d8a
ms.date: 12/05/2018
ms.keywords: IESIsdbCasResponseEvent, IESIsdbCasResponseEvent interface [DirectShow], IESIsdbCasResponseEvent interface [DirectShow],described, mstv.iesisdbcasresponseevent, tuner/IESIsdbCasResponseEvent
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
 - IESIsdbCasResponseEvent
 - tuner/IESIsdbCasResponseEvent
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
 - IESIsdbCasResponseEvent
---

# IESIsdbCasResponseEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) <b>IsdbCasResponse</b> event. An Integrated Services Digital Broadcasting (ISDB) PBDA media transform device (MTD) fires an <b>IsdbCasResponse</b> event after a media sink device (MSD)  calls the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_isdbconditionalaccess-setisdbcasrequest">IBDA_ISDBConditionalAccess::SetIsdbCasRequest</a> method to indicate communication with a conditional access system (CAS) card. The MTD fires the <b>IsdbCasResponse</b> event to signal that response data is available.

## -inheritance

The <b>IESIsdbCasResponseEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>. <b>IESIsdbCasResponseEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESIsdbCasResponseEvent)</code>.
