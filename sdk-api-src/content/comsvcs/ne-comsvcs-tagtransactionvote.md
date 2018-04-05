---
UID: NE:comsvcs.tagTransactionVote
title: tagTransactionVote
author: windows-driver-content
description: Indicates the readiness of an object to commit or abort the current transaction.
old-location: cos\transactionvote.htm
old-project: cossdk
ms.assetid: 2fea9ac5-f714-4682-a78c-bfe9396fccd5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: TransactionVote, TransactionVote enumeration [COM+], TxAbort, TxCommit, _cos_TransactionVote, comsvcs/TransactionVote, comsvcs/TxAbort, comsvcs/TxCommit, cos.transactionvote, tagTransactionVote
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: TransactionVote
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ComSvcs.h
api_name:
-	TransactionVote
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTransactionVote enumeration


## -description


Indicates the readiness of an object to commit or abort the current transaction.


## -enum-fields




### -field TxCommit

An existing object votes to commit the current transaction.


### -field TxAbort

An existing object votes to abort the current transaction.


## -see-also




<a href="https://msdn.microsoft.com/cba54ad7-c670-4efb-ad3b-aca1daabc4a3">IContextState</a>
 

 

