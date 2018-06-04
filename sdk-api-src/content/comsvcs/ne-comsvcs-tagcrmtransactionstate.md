---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

