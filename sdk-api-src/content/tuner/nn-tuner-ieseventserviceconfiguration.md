---
UID: NN:tuner.IESEventServiceConfiguration
title: IESEventServiceConfiguration (tuner.h)
description: Contains methods that configure an event service that implements the IESEventService interface.
helpviewer_keywords: ["IESEventServiceConfiguration","IESEventServiceConfiguration interface [Microsoft TV Technologies]","IESEventServiceConfiguration interface [Microsoft TV Technologies]","described","mstv.ieseventserviceconfiguration","tuner/IESEventServiceConfiguration"]
old-location: mstv\ieseventserviceconfiguration.htm
tech.root: mstv
ms.assetid: 0b901732-42e1-4f50-904c-75d8202bb5b7
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration, IESEventServiceConfiguration interface [Microsoft TV Technologies], IESEventServiceConfiguration interface [Microsoft TV Technologies],described, mstv.ieseventserviceconfiguration, tuner/IESEventServiceConfiguration
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
 - IESEventServiceConfiguration
 - tuner/IESEventServiceConfiguration
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
 - IESEventServiceConfiguration
---

# IESEventServiceConfiguration interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Contains methods that configure an event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface. This interface allows you to create your own event service and set it up to receive events from a Protected Broadcast Driver Architecture (PBDA) event service, then pass those events to your event service's clients.

## -inheritance

The <b>IESEventServiceConfiguration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEventServiceConfiguration</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEventServiceConfiguration)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a>
