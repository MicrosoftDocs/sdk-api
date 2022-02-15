---
UID: NE:comsvcs.tagTransactionVote
title: TransactionVote (comsvcs.h)
description: Indicates the readiness of an object to commit or abort the current transaction.
helpviewer_keywords: ["TransactionVote","TransactionVote enumeration [COM+]","TxAbort","TxCommit","_cos_TransactionVote","comsvcs/TransactionVote","comsvcs/TxAbort","comsvcs/TxCommit","cos.transactionvote"]
old-location: cos\transactionvote.htm
tech.root: cos
ms.assetid: 2fea9ac5-f714-4682-a78c-bfe9396fccd5
ms.date: 12/05/2018
ms.keywords: TransactionVote, TransactionVote enumeration [COM+], TxAbort, TxCommit, _cos_TransactionVote, comsvcs/TransactionVote, comsvcs/TxAbort, comsvcs/TxCommit, cos.transactionvote
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
req.typenames: TransactionVote
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTransactionVote
 - comsvcs/tagTransactionVote
 - TransactionVote
 - comsvcs/TransactionVote
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
 - TransactionVote
---

# TransactionVote enumeration


## -description

Indicates the readiness of an object to commit or abort the current transaction.

## -enum-fields

### -field TxCommit:0

An existing object votes to commit the current transaction.

### -field TxAbort

An existing object votes to abort the current transaction.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>
