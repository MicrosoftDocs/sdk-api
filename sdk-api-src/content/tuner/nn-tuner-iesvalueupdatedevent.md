---
UID: NN:tuner.IESValueUpdatedEvent
title: IESValueUpdatedEvent (tuner.h)
description: Implements an event that Protected Broadcast Driver Architecture (PBDA) Media Transform Devices (MTDs) use to inform a Media Sink Device that the MTD has updated the value for a name-value pair or exposed a new name-value pair.
helpviewer_keywords: ["IESValueUpdatedEvent","IESValueUpdatedEvent interface [Microsoft TV Technologies]","IESValueUpdatedEvent interface [Microsoft TV Technologies]","described","mstv.iesvalueupdatedevent","tuner/IESValueUpdatedEvent"]
old-location: mstv\iesvalueupdatedevent.htm
tech.root: mstv
ms.assetid: 6639c483-aebe-43b4-94cd-494b820c1b14
ms.date: 12/05/2018
ms.keywords: IESValueUpdatedEvent, IESValueUpdatedEvent interface [Microsoft TV Technologies], IESValueUpdatedEvent interface [Microsoft TV Technologies],described, mstv.iesvalueupdatedevent, tuner/IESValueUpdatedEvent
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
 - IESValueUpdatedEvent
 - tuner/IESValueUpdatedEvent
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
 - IESValueUpdatedEvent
---

# IESValueUpdatedEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements an event that Protected Broadcast Driver Architecture (PBDA) Media Transform Devices (MTDs) use to inform a Media Sink Device that the MTD has updated the value for a name-value pair or exposed a new name-value pair. The pair is implemented as part of the PBDA General Purpose Name-Value Service.

## -inheritance

The <b>IESValueUpdatedEvent</b> interface inherits from <b>IESEvent</b>. <b>IESValueUpdatedEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESValueUpdatedEvent)</code>.
