---
UID: NN:comsvcs.IComObjectConstruction2Events
title: IComObjectConstruction2Events (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber if a constructed object is created.
old-location: cos\icomobjectconstruction2events.htm
tech.root: cossdk
ms.assetid: 976b8c1a-5ccd-48e2-a77c-10d4de9a4ffa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectConstruction2Events, IComObjectConstruction2Events interface [COM+], IComObjectConstruction2Events interface [COM+],described, _dtc_icomobjectconstruction2events, comsvcs/IComObjectConstruction2Events, cos.icomobjectconstruction2events
ms.topic: interface
f1_keywords: 
 - "comsvcs/IComObjectConstruction2Events"
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
 - IComObjectConstruction2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectConstruction2Events interface


## -description


Notifies the subscriber if a constructed object is created. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog. A constructed object is derived from the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstruct">IObjectConstruct</a> interface. Constructed objects can inherit parameter names from within other objects or libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectConstruction2Events</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectConstruction2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectConstruction2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectconstruction2events-onobjectconstruct2">OnObjectConstruct2</a>
</td>
<td align="left" width="63%">
Generated when a constructed object is created.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

