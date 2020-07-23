---
UID: NN:comsvcs.IComObjectEvents
title: IComObjectEvents (comsvcs.h)
description: Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed.
helpviewer_keywords: ["IComObjectEvents","IComObjectEvents interface [COM+]","IComObjectEvents interface [COM+]","described","_dtc_IComObjectEvents","comsvcs/IComObjectEvents","cos.icomobjectevents"]
old-location: cos\icomobjectevents.htm
tech.root: cos
ms.assetid: 4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1
ms.date: 12/05/2018
ms.keywords: IComObjectEvents, IComObjectEvents interface [COM+], IComObjectEvents interface [COM+],described, _dtc_IComObjectEvents, comsvcs/IComObjectEvents, cos.icomobjectevents
f1_keywords:
- comsvcs/IComObjectEvents
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
- IComObjectEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectEvents interface


## -description


Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed. The subscriber is notified if <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">IObjectContext::DisableCommit</a>, <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">IObjectContext::EnableCommit</a>, <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">IObjectContext::SetComplete</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">IObjectContext::SetAbort</a> is called. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectevents-ondisablecommit">OnDisableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectevents-onenablecommit">OnEnableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectevents-onobjectactivate">OnObjectActivate</a>
</td>
<td align="left" width="63%">
Generated when an object gets an instance of a new JIT-activated object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectevents-onobjectdeactivate">OnObjectDeactivate</a>
</td>
<td align="left" width="63%">
Generated when the JIT-activated object is freed by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectevents-onsetcomplete">OnSetComplete</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> on a context.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

