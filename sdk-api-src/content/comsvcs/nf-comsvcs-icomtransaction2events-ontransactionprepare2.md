---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionPrepare2
title: IComTransaction2Events::OnTransactionPrepare2
author: windows-sdk-content
description: Generated when the transaction is in the prepare phase of the commit protocol.
old-location: cos\icomtransaction2events_ontransactionprepare2.htm
old-project: cossdk
ms.assetid: 1b2ea10f-7b74-474e-bdf1-040d789fa7c9
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionPrepare2 method, IComTransaction2Events.OnTransactionPrepare2, IComTransaction2Events::OnTransactionPrepare2, OnTransactionPrepare2, OnTransactionPrepare2 method [COM+], OnTransactionPrepare2 method [COM+],IComTransaction2Events interface, _cos_IComTransaction2Events_OnTransactionPrepare2, comsvcs/IComTransaction2Events::OnTransactionPrepare2, cos.icomtransaction2events_ontransactionprepare2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComTransaction2Events.OnTransactionPrepare2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComTransaction2Events::OnTransactionPrepare2


## -description


Generated when the transaction is in the prepare phase of the commit protocol.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


### -param fVoteYes [in]

The resource manager's result concerning the outcome of the prepare phase.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/103776c8-1cdc-46a5-a2ce-54163726e602">IComTransaction2Events</a>
 

 

