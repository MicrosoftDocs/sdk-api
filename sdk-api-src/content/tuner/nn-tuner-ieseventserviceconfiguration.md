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

Contains methods that configure an event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface. This interface allows you to create your own event service and set it up to receive events from a Protected Broadcast Driver Architecture (PBDA) event service, then pass those events to your event service's clients.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESEventServiceConfiguration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IESEventServiceConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESEventServiceConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-removegraph">RemoveGraph</a>
</td>
<td align="left" width="63%">
Removes a PBDA event service from a filter  graph.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-removeowner">RemoveOwner</a>
</td>
<td align="left" width="63%">
Removes the owner of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> event service.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-removeparent">RemoveParent</a>
</td>
<td align="left" width="63%">
Removes the parent of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> event service so that the event service can no longer pass events to the parent.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-setgraph">SetGraph</a>
</td>
<td align="left" width="63%">
Attaches a PBDA event service to a filter  graph.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-setowner">SetOwner</a>
</td>
<td align="left" width="63%">
Specifies the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a> object that an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> event service uses to pass advise events to its parent (the owner).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-setparent">SetParent</a>
</td>
<td align="left" width="63%">
Specifies an event service (the parent) that another <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> event service can pass its events to.
          

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESEventServiceConfiguration)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a>