---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionAbort
title: IComLTxEvents::OnLtxTransactionAbort (comsvcs.h)
description: Generated when a transaction is aborted.helpviewer_keywords: ["IComLTxEvents interface [COM+]","OnLtxTransactionAbort method","IComLTxEvents.OnLtxTransactionAbort","IComLTxEvents::OnLtxTransactionAbort","OnLtxTransactionAbort","OnLtxTransactionAbort method [COM+]","OnLtxTransactionAbort method [COM+]","IComLTxEvents interface","comsvcs/IComLTxEvents::OnLtxTransactionAbort","cos.icomltxevents_onltxtransactionabort"]
old-location: cos\icomltxevents_onltxtransactionabort.htm
tech.root: cossdk
ms.assetid: 49117b74-e84b-497c-ae13-6037e8243e79
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionAbort method, IComLTxEvents.OnLtxTransactionAbort, IComLTxEvents::OnLtxTransactionAbort, OnLtxTransactionAbort, OnLtxTransactionAbort method [COM+], OnLtxTransactionAbort method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionAbort, cos.icomltxevents_onltxtransactionabort
f1_keywords:
- comsvcs/IComLTxEvents.OnLtxTransactionAbort
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IComLTxEvents.OnLtxTransactionAbort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComLTxEvents::OnLtxTransactionAbort


## -description


Generated when a transaction is aborted.

The event ID for this event is EID_LTXABORT.



## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param guidLtx [in]

A GUID that identifies the transaction.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>
 

 

