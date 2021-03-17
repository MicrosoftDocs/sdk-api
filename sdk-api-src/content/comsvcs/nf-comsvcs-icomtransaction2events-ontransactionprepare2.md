---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionPrepare2
title: IComTransaction2Events::OnTransactionPrepare2 (comsvcs.h)
description: Generated when the transaction is in the prepare phase of the commit protocol.
helpviewer_keywords: ["IComTransaction2Events interface [COM+]","OnTransactionPrepare2 method","IComTransaction2Events.OnTransactionPrepare2","IComTransaction2Events::OnTransactionPrepare2","OnTransactionPrepare2","OnTransactionPrepare2 method [COM+]","OnTransactionPrepare2 method [COM+]","IComTransaction2Events interface","_cos_IComTransaction2Events_OnTransactionPrepare2","comsvcs/IComTransaction2Events::OnTransactionPrepare2","cos.icomtransaction2events_ontransactionprepare2"]
old-location: cos\icomtransaction2events_ontransactionprepare2.htm
tech.root: cos
ms.assetid: 1b2ea10f-7b74-474e-bdf1-040d789fa7c9
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionPrepare2 method, IComTransaction2Events.OnTransactionPrepare2, IComTransaction2Events::OnTransactionPrepare2, OnTransactionPrepare2, OnTransactionPrepare2 method [COM+], OnTransactionPrepare2 method [COM+],IComTransaction2Events interface, _cos_IComTransaction2Events_OnTransactionPrepare2, comsvcs/IComTransaction2Events::OnTransactionPrepare2, cos.icomtransaction2events_ontransactionprepare2
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
 - IComTransaction2Events::OnTransactionPrepare2
 - comsvcs/IComTransaction2Events::OnTransactionPrepare2
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
 - IComTransaction2Events.OnTransactionPrepare2
---

# IComTransaction2Events::OnTransactionPrepare2


## -description

Generated when the transaction is in the prepare phase of the commit protocol.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

### -param fVoteYes [in]

The resource manager's result concerning the outcome of the prepare phase.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>