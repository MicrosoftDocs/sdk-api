---
UID: NN:comsvcs.IMtsEvents
title: IMtsEvents (comsvcs.h)
description: Provides methods for obtaining information about the running package and establishing event sinks.
old-location: cos\imtsevents.htm
tech.root: cossdk
ms.assetid: 7db3a373-00d3-480e-8f8e-7e65a468d5dc
ms.date: 12/05/2018
ms.keywords: IMtsEvents, IMtsEvents interface [COM+], IMtsEvents interface [COM+],described, _dtc_IMtsEvents_Interface, comsvcs/IMtsEvents, cos.imtsevents
ms.topic: interface
f1_keywords:
- comsvcs/IMtsEvents
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
- IMtsEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMtsEvents interface


## -description


Provides methods for obtaining information about the running package and establishing event sinks. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsEvents</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMtsEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMtsEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsevents-get_fireevents">get_FireEvents</a>
</td>
<td align="left" width="63%">
Retrieves whether events are enabled or disabled for an event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsevents-get_packageguid">get_PackageGuid</a>
</td>
<td align="left" width="63%">
Retrieves the globally unique identifier (GUID) for the package in which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsevents-get_packagename">get_PackageName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the package in which the instance of the object that implements the <b>IMtsEvents</b> interface is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsevents-getprocessid">GetProcessID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the process in which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsevents-postevent">PostEvent</a>
</td>
<td align="left" width="63%">
Posts a user-defined event to an event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

