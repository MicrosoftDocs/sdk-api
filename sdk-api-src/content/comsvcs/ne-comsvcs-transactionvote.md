---
UID: NE:comsvcs.tagTransactionVote
title: TransactionVote (comsvcs.h)
description: Indicates the readiness of an object to commit or abort the current transaction.
old-location: cos\transactionvote.htm
tech.root: cossdk
ms.assetid: 2fea9ac5-f714-4682-a78c-bfe9396fccd5
ms.date: 12/05/2018
ms.keywords: TransactionVote, TransactionVote enumeration [COM+], TxAbort, TxCommit, _cos_TransactionVote, comsvcs/TransactionVote, comsvcs/TxAbort, comsvcs/TxCommit, cos.transactionvote
f1_keywords:
- comsvcs/TransactionVote
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ComSvcs.h
api_name:
- TransactionVote
targetos: Windows
req.typenames: TransactionVote
req.redist: 
ms.custom: 19H1
---

# TransactionVote enumeration


## -description


Indicates the readiness of an object to commit or abort the current transaction.


## -enum-fields




### -field TxCommit

An existing object votes to commit the current transaction.


### -field TxAbort

An existing object votes to abort the current transaction.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icontextstate">IContextState</a>
 

 

