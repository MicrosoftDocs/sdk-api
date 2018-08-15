---
UID: NN:wbemprov.IWbemEventSink
title: IWbemEventSink
author: windows-sdk-content
description: Initiates communication with an event provider using a restricted set of queries.
old-location: wmi\iwbemeventsink.htm
old-project: WmiSdk
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IWbemEventSink, IWbemEventSink interface [Windows Management Instrumentation], IWbemEventSink interface [Windows Management Instrumentation],described, _hmm_iwbemeventsink, wbemprov/IWbemEventSink, wmi.iwbemeventsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventSink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemEventSink interface


## -description


The 
<b>IWbemEventSink</b> interface initiates communication with an event provider using a restricted set of queries. This interface extends 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>, providing new methods dealing with security and performance. For more information about using this interface, see <a href="https://msdn.microsoft.com/075bdc65-4ea3-4f91-9823-1d2d0dc13423">Writing an Event Provider</a> and <a href="https://msdn.microsoft.com/86eaeb5c-c27e-4794-88e2-e0ffbb885290">Securing WMI Events</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventSink</b> interface has these types of members:
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
<a href="https://msdn.microsoft.com/f72ab8f7-e4de-4f64-80db-6981b0bd13d3">GetRestrictedSink</a>
</td>
<td align="left" width="63%">
Called by the consumer to set up restricted event queries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc5afbc1-60da-42ec-9dc3-79b66243690c">IsActive</a>
</td>
<td align="left" width="63%">
Checks status of event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fcc1598-bc0c-4d4a-ad6f-69317bd789a4">SetBatchingParameters</a>
</td>
<td align="left" width="63%">
Called by the consumer to set batching parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/887b3c21-2ff6-4ae9-80bf-19f601da5e8b">SetSinkSecurity</a>
</td>
<td align="left" width="63%">
Used to update the security descriptor on an event sink.

</td>
</tr>
</table> 


## -remarks



When implementing an event subscription sink (<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> or <b>IWbemEventSink</b>), do  not call into WMI from within the  methods on the sink object.  For example, calling <a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">IWbemServices::CancelAsyncCall</a> to cancel the sink  from within an implementation of <a href="https://msdn.microsoft.com/887b3c21-2ff6-4ae9-80bf-19f601da5e8b">IWbemEventSink::SetSinkSecurity</a> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.




## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>
 

 

