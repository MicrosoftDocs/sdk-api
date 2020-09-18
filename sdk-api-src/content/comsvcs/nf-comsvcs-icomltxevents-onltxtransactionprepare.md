---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionPrepare
title: IComLTxEvents::OnLtxTransactionPrepare (comsvcs.h)
description: Generated when COM+ receives a prepare notification for a transaction.
helpviewer_keywords: ["IComLTxEvents interface [COM+]","OnLtxTransactionPrepare method","IComLTxEvents.OnLtxTransactionPrepare","IComLTxEvents::OnLtxTransactionPrepare","OnLtxTransactionPrepare","OnLtxTransactionPrepare method [COM+]","OnLtxTransactionPrepare method [COM+]","IComLTxEvents interface","comsvcs/IComLTxEvents::OnLtxTransactionPrepare","cos.icomltxevents_onltxtransactionprepare"]
old-location: cos\icomltxevents_onltxtransactionprepare.htm
tech.root: cos
ms.assetid: 31915d4c-7ac0-406b-b2d2-ab96b317be3f
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionPrepare method, IComLTxEvents.OnLtxTransactionPrepare, IComLTxEvents::OnLtxTransactionPrepare, OnLtxTransactionPrepare, OnLtxTransactionPrepare method [COM+], OnLtxTransactionPrepare method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionPrepare, cos.icomltxevents_onltxtransactionprepare
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
 - IComLTxEvents::OnLtxTransactionPrepare
 - comsvcs/IComLTxEvents::OnLtxTransactionPrepare
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
 - IComLTxEvents.OnLtxTransactionPrepare
---

# IComLTxEvents::OnLtxTransactionPrepare


## -description

Generated when COM+ receives a prepare notification for a transaction.

The event ID for this event is EID_LTXPREPARE.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidLtx [in]

A GUID that identifies the transaction.

### -param fVote [in]

The COM+ vote for the prepare request.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>