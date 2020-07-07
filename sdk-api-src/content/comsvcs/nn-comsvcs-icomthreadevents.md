---
UID: NN:comsvcs.IComThreadEvents
title: IComThreadEvents (comsvcs.h)
description: Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated.
helpviewer_keywords: ["IComThreadEvents","IComThreadEvents interface [COM+]","IComThreadEvents interface [COM+]","described","_dtc_IComThreadEvents","comsvcs/IComThreadEvents","cos.icomthreadevents"]
old-location: cos\icomthreadevents.htm
tech.root: cossdk
ms.assetid: a6523088-cca4-41c1-a3fe-d8cb7320ff33
ms.date: 12/05/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], IComThreadEvents interface [COM+],described, _dtc_IComThreadEvents, comsvcs/IComThreadEvents, cos.icomthreadevents
f1_keywords:
- comsvcs/IComThreadEvents
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- ComSvcs.h
api_name:
- IComThreadEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComThreadEvents interface


## -description


Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated. The subscriber is also notified if an activity is assigned or unassigned to an apartment thread. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComThreadEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComThreadEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComThreadEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadassignapartment">OnThreadAssignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is assigned to an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadbindtoapartment">OnThreadBindToApartment</a>
</td>
<td align="left" width="63%">
Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadstart">OnThreadStart</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadterminate">OnThreadTerminate</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadunassignapartment">OnThreadUnassignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is unassigned from an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomthreadevents-onthreadunbind">OnThreadUnBind</a>
</td>
<td align="left" width="63%">
Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

