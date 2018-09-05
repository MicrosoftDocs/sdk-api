---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionPrepare
title: IComTransactionEvents::OnTransactionPrepare
author: windows-sdk-content
description: Generated when the prepare phase of the two-phase commit protocol of the transaction is completed.
old-location: cos\icomtransactionevents_ontransactionprepare.htm
old-project: cossdk
ms.assetid: ab56c3fc-daeb-4c7a-ac7f-a2c6d70c1006
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionPrepare method, IComTransactionEvents.OnTransactionPrepare, IComTransactionEvents::OnTransactionPrepare, OnTransactionPrepare, OnTransactionPrepare method [COM+], OnTransactionPrepare method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionPrepare, comsvcs/IComTransactionEvents::OnTransactionPrepare, cos.icomtransactionevents_ontransactionprepare
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTransactionEvents.OnTransactionPrepare
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComTransactionEvents::OnTransactionPrepare


## -description


Generated when the prepare phase of the two-phase commit protocol of the transaction is completed.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


### -param fVoteYes [in]

The resource managers result concerning the outcome of the prepare phase.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3">IComTransactionEvents</a>
 

 

