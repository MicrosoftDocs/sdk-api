---
UID: NN:wbemprov.IWbemEventConsumerProvider
title: IWbemEventConsumerProvider (wbemprov.h)
description: Provides the primary interface for an event consumer provider. Through this interface and the FindConsumer method, an event consumer provider can indicate which event consumers should receive a given event.
helpviewer_keywords: ["IWbemEventConsumerProvider","IWbemEventConsumerProvider interface [Windows Management Instrumentation]","IWbemEventConsumerProvider interface [Windows Management Instrumentation]","described","_hmm_iwbemeventconsumerprovider","wbemprov/IWbemEventConsumerProvider","wmi.iwbemeventconsumerprovider"]
old-location: wmi\iwbemeventconsumerprovider.htm
tech.root: wmi
ms.assetid: 793bbc22-4a8b-4ab3-8cfe-7d81f42a6b7f
ms.date: 12/05/2018
ms.keywords: IWbemEventConsumerProvider, IWbemEventConsumerProvider interface [Windows Management Instrumentation], IWbemEventConsumerProvider interface [Windows Management Instrumentation],described, _hmm_iwbemeventconsumerprovider, wbemprov/IWbemEventConsumerProvider, wmi.iwbemeventconsumerprovider
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemEventConsumerProvider
 - wbemprov/IWbemEventConsumerProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventConsumerProvider
---

# IWbemEventConsumerProvider interface


## -description

The 
<b>IWbemEventConsumerProvider</b> interface provides the primary interface for an event consumer provider. Through 
this interface and the 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer">FindConsumer</a> method, an event consumer provider can indicate which event consumers should receive a given event. The first time WMI delivers an event to a particular consumer, WMI calls 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer">FindConsumer</a> to retrieve a pointer to the sink for that physical consumer. WMI then sends all subsequent occurrences of the event the sink provided by 
<b>FindConsumer</b>.

If you implement a permanent event consumer, you must implement 
<b>IWbemEventConsumerProvider</b> so that WMI can deliver events to your physical consumer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventConsumerProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemEventConsumerProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemEventConsumerProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer">FindConsumer</a>
</td>
<td align="left" width="63%">
Called by Windows Management to retrieve an 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemunboundobjectsink">IWbemUnboundObjectSink</a> object for a particular logical consumer.

</td>
</tr>
</table>