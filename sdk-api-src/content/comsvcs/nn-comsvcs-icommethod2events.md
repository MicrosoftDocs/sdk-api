---
UID: NN:comsvcs.IComMethod2Events
title: IComMethod2Events (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception.
old-location: cos\icommethod2events.htm
tech.root: cossdk
ms.assetid: e0642cb2-d5f2-4e4b-ad35-7818983ed467
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComMethod2Events, IComMethod2Events interface [COM+], IComMethod2Events interface [COM+],described, _dtc_IComMethod2Events, comsvcs/IComMethod2Events, cos.icommethod2events
ms.topic: interface
f1_keywords: ["comsvcs/IComMethod2Events"]
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
 - IComMethod2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComMethod2Events interface


## -description


Notifies the subscriber if an object's method has been called, returned, or generated an exception. This interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a> interface to provide thread information. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComMethod2Events</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComMethod2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComMethod2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethod2events-onmethodcall2">OnMethodCall2</a>
</td>
<td align="left" width="63%">
Generated when an object's method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethod2events-onmethodexception2">OnMethodException2</a>
</td>
<td align="left" width="63%">
Generated when an object's method generates an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icommethod2events-onmethodreturn2">OnMethodReturn2</a>
</td>
<td align="left" width="63%">
Generated when an object's method returns.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

