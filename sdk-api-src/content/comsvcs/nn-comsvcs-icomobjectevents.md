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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComObjectEvents
 - comsvcs/IComObjectEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComObjectEvents
---

# IComObjectEvents interface


## -description

Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed. The subscriber is notified if <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">IObjectContext::DisableCommit</a>, <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">IObjectContext::EnableCommit</a>, <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">IObjectContext::SetComplete</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">IObjectContext::SetAbort</a> is called. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComObjectEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
