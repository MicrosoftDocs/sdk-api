---
UID: NN:comsvcs.IComActivityEvents
title: IComActivityEvents (comsvcs.h)
description: Notifies the subscriber if an activity is created, destroyed, or timed out.
old-location: cos\icomactivityevents.htm
tech.root: cossdk
ms.assetid: 9b702bcd-d5a6-41fa-98ce-00a245dfe770
ms.date: 12/05/2018
ms.keywords: IComActivityEvents, IComActivityEvents interface [COM+], IComActivityEvents interface [COM+],described, _dtc_IComActivityEvents, comsvcs/IComActivityEvents, cos.icomactivityevents
ms.topic: interface
f1_keywords:
- comsvcs/IComActivityEvents
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
- IComActivityEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComActivityEvents interface


## -description


Notifies the subscriber if an activity is created, destroyed, or timed out. The activity event is published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComActivityEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComActivityEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComActivityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivitycreate">OnActivityCreate</a>
</td>
<td align="left" width="63%">
Generated when an activity starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivitydestroy">OnActivityDestroy</a>
</td>
<td align="left" width="63%">
Generated when an activity is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivityenter">OnActivityEnter</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is entered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivityleave">OnActivityLeave</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is left.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivityleavesame">OnActivityLeaveSame</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is left after being entered recursively.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivityreenter">OnActivityReenter</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is reentered recursively.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomactivityevents-onactivitytimeout">OnActivityTimeout</a>
</td>
<td align="left" width="63%">
Generated when a call into an activity times out.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

