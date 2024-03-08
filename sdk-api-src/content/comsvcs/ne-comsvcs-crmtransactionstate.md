---
UID: NE:comsvcs.tagCrmTransactionState
title: CrmTransactionState (comsvcs.h)
description: Represents the current transaction state of the transaction.
helpviewer_keywords: ["CrmTransactionState","CrmTransactionState enumeration [COM+]","TxState_Aborted","TxState_Active","TxState_Committed","TxState_Indoubt","_cos_CrmTransactionState","comsvcs/CrmTransactionState","comsvcs/TxState_Aborted","comsvcs/TxState_Active","comsvcs/TxState_Committed","comsvcs/TxState_Indoubt","cos.crmtransactionstate"]
old-location: cos\crmtransactionstate.htm
tech.root: cos
ms.assetid: ae096ba2-3347-4d8c-89af-ee4517554a91
ms.date: 12/05/2018
ms.keywords: CrmTransactionState, CrmTransactionState enumeration [COM+], TxState_Aborted, TxState_Active, TxState_Committed, TxState_Indoubt, _cos_CrmTransactionState, comsvcs/CrmTransactionState, comsvcs/TxState_Aborted, comsvcs/TxState_Active, comsvcs/TxState_Committed, comsvcs/TxState_Indoubt, cos.crmtransactionstate
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
req.typenames: CrmTransactionState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCrmTransactionState
 - comsvcs/tagCrmTransactionState
 - CrmTransactionState
 - comsvcs/CrmTransactionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CrmTransactionState
---

# CrmTransactionState enumeration


## -description

Represents the current transaction state of the transaction.

## -enum-fields

### -field TxState_Active:0

The transaction is active.

### -field TxState_Committed

The transaction is committed.

### -field TxState_Aborted

The transaction was aborted.

### -field TxState_Indoubt

The transaction is in doubt.

## -see-also

<a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmmonitorlogrecords-get_transactionstate">ICrmMonitorLogRecords::get_TransactionState</a>
