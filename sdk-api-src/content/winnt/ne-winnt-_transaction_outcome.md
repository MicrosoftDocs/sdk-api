---
UID: NE:winnt._TRANSACTION_OUTCOME
title: "_TRANSACTION_OUTCOME"
author: windows-sdk-content
description: Defines the outcomes (results) that KTM can assign to a transaction.
old-location: fs\transaction_outcome.htm
tech.root: Ktm
ms.assetid: d4315a62-b65f-4744-8084-2317ad39c32c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TRANSACTION_OUTCOME, TRANSACTION_OUTCOME enumeration [Files], TransactionOutcomeAborted, TransactionOutcomeCommitted, TransactionOutcomeUndetermined, _TRANSACTION_OUTCOME, fs.transaction_outcome, winnt/TRANSACTION_OUTCOME, winnt/TransactionOutcomeAborted, winnt/TransactionOutcomeCommitted, winnt/TransactionOutcomeUndetermined
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: TRANSACTION_OUTCOME
req.redist: 
---

# _TRANSACTION_OUTCOME enumeration


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




<a href="https://msdn.microsoft.com/85a79698-a1ae-45a4-805e-25175034fa65">About KTM</a>



<a href="https://msdn.microsoft.com/6441fa83-1e60-4257-b1b2-41f87ce0dd85">KTM Reference</a>
 

 

