---
UID: NN:comsvcs.IComTransaction2Events
title: IComTransaction2Events (comsvcs.h)
description: Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol.
helpviewer_keywords: ["IComTransaction2Events","IComTransaction2Events interface [COM+]","IComTransaction2Events interface [COM+]","described","_dtc_icomtransaction2events","comsvcs/IComTransaction2Events","cos.icomtransaction2events"]
old-location: cos\icomtransaction2events.htm
tech.root: cos
ms.assetid: 103776c8-1cdc-46a5-a2ce-54163726e602
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events, IComTransaction2Events interface [COM+], IComTransaction2Events interface [COM+],described, _dtc_icomtransaction2events, comsvcs/IComTransaction2Events, cos.icomtransaction2events
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
 - IComTransaction2Events
 - comsvcs/IComTransaction2Events
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
 - IComTransaction2Events
---

# IComTransaction2Events interface


## -description

Notifies the subscriber if a Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the transaction is in the prepare phase of the two-phase commit protocol. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComTransaction2Events</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComTransaction2Events</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>



<a href="/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>
