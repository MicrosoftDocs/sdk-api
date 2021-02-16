---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionCommit
title: IComLTxEvents::OnLtxTransactionCommit (comsvcs.h)
description: Generated when a transaction is committed.
helpviewer_keywords: ["IComLTxEvents interface [COM+]","OnLtxTransactionCommit method","IComLTxEvents.OnLtxTransactionCommit","IComLTxEvents::OnLtxTransactionCommit","OnLtxTransactionCommit","OnLtxTransactionCommit method [COM+]","OnLtxTransactionCommit method [COM+]","IComLTxEvents interface","comsvcs/IComLTxEvents::OnLtxTransactionCommit","cos.icomltxevents_onltxtransactioncommit"]
old-location: cos\icomltxevents_onltxtransactioncommit.htm
tech.root: cos
ms.assetid: c3462a79-6056-4a57-b971-78d8b4bd2a70
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionCommit method, IComLTxEvents.OnLtxTransactionCommit, IComLTxEvents::OnLtxTransactionCommit, OnLtxTransactionCommit, OnLtxTransactionCommit method [COM+], OnLtxTransactionCommit method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionCommit, cos.icomltxevents_onltxtransactioncommit
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
 - IComLTxEvents::OnLtxTransactionCommit
 - comsvcs/IComLTxEvents::OnLtxTransactionCommit
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
 - IComLTxEvents.OnLtxTransactionCommit
---

# IComLTxEvents::OnLtxTransactionCommit


## -description

Generated when a transaction is committed.

The event ID for this event is EID_LTXCOMMIT.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidLtx [in]

A GUID that identifies the transaction.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>