---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionStart
title: IComLTxEvents::OnLtxTransactionStart
author: windows-sdk-content
description: Generated when a transaction is started.
old-location: cos\icomltxevents_onltxtransactionstart.htm
old-project: cossdk
ms.assetid: 0d063e3f-d7f8-45b1-995f-29903c42ec37
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionStart method, IComLTxEvents.OnLtxTransactionStart, IComLTxEvents::OnLtxTransactionStart, OnLtxTransactionStart, OnLtxTransactionStart method [COM+], OnLtxTransactionStart method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionStart, cos.icomltxevents_onltxtransactionstart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComLTxEvents.OnLtxTransactionStart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComLTxEvents::OnLtxTransactionStart


## -description


Generated when a transaction is started.

The event ID for this event is EID_LTXSTART.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidLtx [in]

A GUID that identifies the transaction.


### -param tsid [in]

A GUID that identifies the COM+ transaction context.


### -param fRoot [in]

Indicates whether the COM+ transaction context is a root transaction context.


### -param nIsolationLevel [in]

The transaction isolation level of the root COM+ transactional context.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/8be6dddb-ed57-4715-8933-8a0e478095c8">IComLTxEvents</a>
 

 

