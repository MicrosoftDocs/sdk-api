---
UID: NN:comsvcs.IComTransactionEvents
title: IComTransactionEvents (comsvcs.h)
description: Notifies the subscriber if the Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts.
helpviewer_keywords: ["IComTransactionEvents","IComTransactionEvents interface [COM+]","IComTransactionEvents interface [COM+]","described","_dtc_IComTransactionEvents","comsvcs/IComTransactionEvents","cos.icomtransactionevents"]
old-location: cos\icomtransactionevents.htm
tech.root: cos
ms.assetid: f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3
ms.date: 12/05/2018
ms.keywords: IComTransactionEvents, IComTransactionEvents interface [COM+], IComTransactionEvents interface [COM+],described, _dtc_IComTransactionEvents, comsvcs/IComTransactionEvents, cos.icomtransactionevents
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
 - IComTransactionEvents
 - comsvcs/IComTransactionEvents
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
 - IComTransactionEvents
---

# IComTransactionEvents interface


## -description

Notifies the subscriber if the Microsoft Distributed Transaction Coordinator (DTC) transaction starts, commits, or aborts. The subscriber is also notified when the resource manager retrieves prepare information from the transaction manager. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComTransactionEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComTransactionEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>



<a href="/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>
