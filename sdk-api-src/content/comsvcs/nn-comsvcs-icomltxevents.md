---
UID: NN:comsvcs.IComLTxEvents
title: IComLTxEvents (comsvcs.h)
description: Notifies the subscriber of events that relate to COM+ transactions.
helpviewer_keywords: ["IComLTxEvents","IComLTxEvents interface [COM+]","IComLTxEvents interface [COM+]","described","comsvcs/IComLTxEvents","cos.icomltxevents"]
old-location: cos\icomltxevents.htm
tech.root: cos
ms.assetid: 8be6dddb-ed57-4715-8933-8a0e478095c8
ms.date: 12/05/2018
ms.keywords: IComLTxEvents, IComLTxEvents interface [COM+], IComLTxEvents interface [COM+],described, comsvcs/IComLTxEvents, cos.icomltxevents
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - IComLTxEvents
 - comsvcs/IComLTxEvents
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
 - IComLTxEvents
---

# IComLTxEvents interface


## -description

Notifies the subscriber of events that relate to COM+ transactions. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComLTxEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComLTxEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
