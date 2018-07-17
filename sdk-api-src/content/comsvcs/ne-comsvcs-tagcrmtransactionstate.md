---
UID: NE:comsvcs.tagCrmTransactionState
title: tagCrmTransactionState
author: windows-sdk-content
description: Represents the current transaction state of the transaction.
old-location: cos\crmtransactionstate.htm
old-project: cossdk
ms.assetid: ae096ba2-3347-4d8c-89af-ee4517554a91
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CrmTransactionState, CrmTransactionState enumeration [COM+], TxState_Aborted, TxState_Active, TxState_Committed, TxState_Indoubt, _cos_CrmTransactionState, comsvcs/CrmTransactionState, comsvcs/TxState_Aborted, comsvcs/TxState_Active, comsvcs/TxState_Committed, comsvcs/TxState_Indoubt, cos.crmtransactionstate, tagCrmTransactionState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CrmTransactionState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CrmTransactionState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCrmTransactionState enumeration


## -description


Represents the current transaction state of the transaction.


## -enum-fields




### -field TxState_Active

The transaction is active.


### -field TxState_Committed

The transaction is committed.


### -field TxState_Aborted

The transaction was aborted.


### -field TxState_Indoubt

The transaction is in doubt.


## -see-also




<a href="https://msdn.microsoft.com/9aaa3d6c-41b9-4661-8e7e-ef1d1abba4aa">ICrmMonitorLogRecords::get_TransactionState</a>
 

 

