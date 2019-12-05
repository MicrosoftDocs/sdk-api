---
UID: NN:comsvcs.IComMethodEvents
title: IComMethodEvents (comsvcs.h)
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception.
old-location: cos\icommethodevents.htm
tech.root: cossdk
ms.assetid: 24670a23-4300-48f9-a089-dff3082cb544
ms.date: 12/05/2018
ms.keywords: IComMethodEvents, IComMethodEvents interface [COM+], IComMethodEvents interface [COM+],described, _dtc_IComMethodEvents, comsvcs/IComMethodEvents, cos.icommethodevents
ms.topic: interface
f1_keywords:
- comsvcs/IComMethodEvents
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
- IComMethodEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComMethodEvents interface


## -description


Notifies the subscriber if an object's method has been called, returned, or generated an exception. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComMethodEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComMethodEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComMethodEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethodevents-onmethodcall">OnMethodCall</a>
</td>
<td align="left" width="63%">
Generated when an object's method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethodevents-onmethodexception">OnMethodException</a>
</td>
<td align="left" width="63%">
Generated when an object's method generates an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethodevents-onmethodreturn">OnMethodReturn</a>
</td>
<td align="left" width="63%">
Generated when an object's method returns.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

