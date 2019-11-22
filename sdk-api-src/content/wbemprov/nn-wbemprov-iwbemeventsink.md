---
UID: NN:wbemprov.IWbemEventSink
title: IWbemEventSink (wbemprov.h)

description: Initiates communication with an event provider using a restricted set of queries.
old-location: wmi\iwbemeventsink.htm
tech.root: WmiSdk
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464

ms.date: 12/05/2018
ms.keywords: IWbemEventSink, IWbemEventSink interface [Windows Management Instrumentation], IWbemEventSink interface [Windows Management Instrumentation],described, _hmm_iwbemeventsink, wbemprov/IWbemEventSink, wmi.iwbemeventsink
ms.topic: interface
f1_keywords: 
 - "wbemprov/IWbemEventSink"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemEventSink interface


## -description


The 
<b>IWbemEventSink</b> interface initiates communication with an event provider using a restricted set of queries. This interface extends 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>, providing new methods dealing with security and performance. For more information about using this interface, see <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/writing-an-event-provider">Writing an Event Provider</a> and <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/securing-wmi-events">Securing WMI Events</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink">GetRestrictedSink</a>
</td>
<td align="left" width="63%">
Called by the consumer to set up restricted event queries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-isactive">IsActive</a>
</td>
<td align="left" width="63%">
Checks status of event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters">SetBatchingParameters</a>
</td>
<td align="left" width="63%">
Called by the consumer to set batching parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity">SetSinkSecurity</a>
</td>
<td align="left" width="63%">
Used to update the security descriptor on an event sink.

</td>
</tr>
</table> 


## -remarks



When implementing an event subscription sink (<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> or <b>IWbemEventSink</b>), do  not call into WMI from within the  methods on the sink object.  For example, calling <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">IWbemServices::CancelAsyncCall</a> to cancel the sink  from within an implementation of <a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity">IWbemEventSink::SetSinkSecurity</a> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>
 

 

