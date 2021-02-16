---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionPrepare
title: IComTransactionEvents::OnTransactionPrepare (comsvcs.h)
description: Generated when the prepare phase of the two-phase commit protocol of the transaction is completed.
helpviewer_keywords: ["IComTransactionEvents interface [COM+]","OnTransactionPrepare method","IComTransactionEvents.OnTransactionPrepare","IComTransactionEvents::OnTransactionPrepare","OnTransactionPrepare","OnTransactionPrepare method [COM+]","OnTransactionPrepare method [COM+]","IComTransactionEvents interface","_dtc_IComTransactionEvents_OnTransactionPrepare","comsvcs/IComTransactionEvents::OnTransactionPrepare","cos.icomtransactionevents_ontransactionprepare"]
old-location: cos\icomtransactionevents_ontransactionprepare.htm
tech.root: cos
ms.assetid: ab56c3fc-daeb-4c7a-ac7f-a2c6d70c1006
ms.date: 12/05/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionPrepare method, IComTransactionEvents.OnTransactionPrepare, IComTransactionEvents::OnTransactionPrepare, OnTransactionPrepare, OnTransactionPrepare method [COM+], OnTransactionPrepare method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionPrepare, comsvcs/IComTransactionEvents::OnTransactionPrepare, cos.icomtransactionevents_ontransactionprepare
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
 - IComTransactionEvents::OnTransactionPrepare
 - comsvcs/IComTransactionEvents::OnTransactionPrepare
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
 - IComTransactionEvents.OnTransactionPrepare
---

# IComTransactionEvents::OnTransactionPrepare


## -description

Generated when the prepare phase of the two-phase commit protocol of the transaction is completed.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

### -param fVoteYes [in]

The resource managers result concerning the outcome of the prepare phase.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransactionevents">IComTransactionEvents</a>