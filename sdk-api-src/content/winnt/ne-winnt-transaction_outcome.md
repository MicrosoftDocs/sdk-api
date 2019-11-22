---
UID: NE:winnt._TRANSACTION_OUTCOME
title: TRANSACTION_OUTCOME (winnt.h)

description: Defines the outcomes (results) that KTM can assign to a transaction.
old-location: fs\transaction_outcome.htm
tech.root: ktm
ms.assetid: d4315a62-b65f-4744-8084-2317ad39c32c

ms.date: 12/05/2018
ms.keywords: TRANSACTION_OUTCOME, TRANSACTION_OUTCOME enumeration [Files], TransactionOutcomeAborted, TransactionOutcomeCommitted, TransactionOutcomeUndetermined, fs.transaction_outcome, winnt/TRANSACTION_OUTCOME, winnt/TransactionOutcomeAborted, winnt/TransactionOutcomeCommitted, winnt/TransactionOutcomeUndetermined
ms.topic: enum
f1_keywords: 
 - "winnt/TRANSACTION_OUTCOME"
dev_langs:
 - c++
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Winnt.h
api_name:
 - TRANSACTION_OUTCOME
targetos: Windows
req.typenames: TRANSACTION_OUTCOME
req.redist: 
ms.custom: 19H1
---

# TRANSACTION_OUTCOME enumeration


## -description


Defines the outcomes (results) that KTM can assign to a transaction.


## -enum-fields




### -field TransactionOutcomeUndetermined

The transaction has not yet been committed or rolled back.


### -field TransactionOutcomeCommitted

The transaction has been committed.


### -field TransactionOutcomeAborted

The transaction has been rolled back.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Ktm/about-ktm">About KTM</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/ktm-reference">KTM Reference</a>
 

 

