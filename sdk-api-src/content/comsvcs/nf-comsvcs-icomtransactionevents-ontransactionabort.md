---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionAbort
title: IComTransactionEvents::OnTransactionAbort method
author: windows-driver-content
description: Generated when a transaction aborts.
old-location: cos\icomtransactionevents_ontransactionabort.htm
old-project: cossdk
ms.assetid: 1dfba278-f733-486e-8bd2-f9dec0736e68
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IComTransactionEvents, IComTransactionEvents interface [COM+], OnTransactionAbort method, IComTransactionEvents::OnTransactionAbort, OnTransactionAbort method [COM+], OnTransactionAbort method [COM+], IComTransactionEvents interface, OnTransactionAbort,IComTransactionEvents.OnTransactionAbort, _dtc_IComTransactionEvents_OnTransactionAbort, comsvcs/IComTransactionEvents::OnTransactionAbort, cos.icomtransactionevents_ontransactionabort
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IComTransactionEvents.OnTransactionAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComTransactionEvents::OnTransactionAbort method


## -description


Generated when a transaction aborts.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3">IComTransactionEvents</a>
 

 

