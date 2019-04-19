---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionPromote
title: IComLTxEvents::OnLtxTransactionPromote (comsvcs.h)
author: windows-sdk-content
description: Generated when a transaction is promoted.
old-location: cos\icomltxevents_onltxtransactionpromote.htm
tech.root: cossdk
ms.assetid: 9cd9927c-355c-4d9f-b679-278e4b6897e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionPromote method, IComLTxEvents.OnLtxTransactionPromote, IComLTxEvents::OnLtxTransactionPromote, OnLtxTransactionPromote, OnLtxTransactionPromote method [COM+], OnLtxTransactionPromote method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionPromote, cos.icomltxevents_onltxtransactionpromote
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
 - IComLTxEvents.OnLtxTransactionPromote
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComLTxEvents::OnLtxTransactionPromote


## -description


Generated when a transaction is promoted.

The event ID for this event is EID_LTXPROMOTE.



## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidLtx [in]

A GUID that identifies the original transaction.


### -param txnId [in]

A GUID that identifies the promoted transaction.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/8be6dddb-ed57-4715-8933-8a0e478095c8">IComLTxEvents</a>
 

 

