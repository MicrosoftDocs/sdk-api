---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionAbort
title: IComTransactionEvents::OnTransactionAbort (comsvcs.h)
description: Generated when a transaction aborts.
old-location: cos\icomtransactionevents_ontransactionabort.htm
tech.root: cossdk
ms.assetid: 1dfba278-f733-486e-8bd2-f9dec0736e68
ms.date: 12/05/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionAbort method, IComTransactionEvents.OnTransactionAbort, IComTransactionEvents::OnTransactionAbort, OnTransactionAbort, OnTransactionAbort method [COM+], OnTransactionAbort method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionAbort, comsvcs/IComTransactionEvents::OnTransactionAbort, cos.icomtransactionevents_ontransactionabort
f1_keywords:
- comsvcs/IComTransactionEvents.OnTransactionAbort
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
- COM
api_location:
- ComSvcs.h
api_name:
- IComTransactionEvents.OnTransactionAbort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTransactionEvents::OnTransactionAbort


## -description


Generated when a transaction aborts.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomtransactionevents">IComTransactionEvents</a>
 

 

