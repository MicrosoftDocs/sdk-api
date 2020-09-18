---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionPromote
title: IComLTxEvents::OnLtxTransactionPromote (comsvcs.h)
description: Generated when a transaction is promoted.
helpviewer_keywords: ["IComLTxEvents interface [COM+]","OnLtxTransactionPromote method","IComLTxEvents.OnLtxTransactionPromote","IComLTxEvents::OnLtxTransactionPromote","OnLtxTransactionPromote","OnLtxTransactionPromote method [COM+]","OnLtxTransactionPromote method [COM+]","IComLTxEvents interface","comsvcs/IComLTxEvents::OnLtxTransactionPromote","cos.icomltxevents_onltxtransactionpromote"]
old-location: cos\icomltxevents_onltxtransactionpromote.htm
tech.root: cos
ms.assetid: 9cd9927c-355c-4d9f-b679-278e4b6897e1
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionPromote method, IComLTxEvents.OnLtxTransactionPromote, IComLTxEvents::OnLtxTransactionPromote, OnLtxTransactionPromote, OnLtxTransactionPromote method [COM+], OnLtxTransactionPromote method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionPromote, cos.icomltxevents_onltxtransactionpromote
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComLTxEvents::OnLtxTransactionPromote
 - comsvcs/IComLTxEvents::OnLtxTransactionPromote
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComLTxEvents.OnLtxTransactionPromote
---

# IComLTxEvents::OnLtxTransactionPromote


## -description

Generated when a transaction is promoted.

The event ID for this event is EID_LTXPROMOTE.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidLtx [in]

A GUID that identifies the original transaction.

### -param txnId [in]

A GUID that identifies the promoted transaction.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>