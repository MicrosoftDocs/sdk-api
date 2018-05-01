---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionAbort
title: IComLTxEvents::OnLtxTransactionAbort method
author: windows-driver-content
description: Generated when a transaction is aborted.
old-location: cos\icomltxevents_onltxtransactionabort.htm
old-project: cossdk
ms.assetid: 49117b74-e84b-497c-ae13-6037e8243e79
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComLTxEvents, IComLTxEvents interface [COM+], OnLtxTransactionAbort method, IComLTxEvents::OnLtxTransactionAbort, OnLtxTransactionAbort method [COM+], OnLtxTransactionAbort method [COM+], IComLTxEvents interface, OnLtxTransactionAbort,IComLTxEvents.OnLtxTransactionAbort, comsvcs/IComLTxEvents::OnLtxTransactionAbort, cos.icomltxevents_onltxtransactionabort
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IComLTxEvents.OnLtxTransactionAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComLTxEvents::OnLtxTransactionAbort method


## -description


Generated when a transaction is aborted.

The event ID for this event is EID_LTXABORT.



## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidLtx [in]

A GUID that identifies the transaction.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/8be6dddb-ed57-4715-8933-8a0e478095c8">IComLTxEvents</a>
 

 

