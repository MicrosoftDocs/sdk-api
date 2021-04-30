---
UID: NF:comsvcs.IComLTxEvents.OnLtxTransactionStart
title: IComLTxEvents::OnLtxTransactionStart (comsvcs.h)
description: Generated when a transaction is started.
helpviewer_keywords: ["IComLTxEvents interface [COM+]","OnLtxTransactionStart method","IComLTxEvents.OnLtxTransactionStart","IComLTxEvents::OnLtxTransactionStart","OnLtxTransactionStart","OnLtxTransactionStart method [COM+]","OnLtxTransactionStart method [COM+]","IComLTxEvents interface","comsvcs/IComLTxEvents::OnLtxTransactionStart","cos.icomltxevents_onltxtransactionstart"]
old-location: cos\icomltxevents_onltxtransactionstart.htm
tech.root: cos
ms.assetid: 0d063e3f-d7f8-45b1-995f-29903c42ec37
ms.date: 12/05/2018
ms.keywords: IComLTxEvents interface [COM+],OnLtxTransactionStart method, IComLTxEvents.OnLtxTransactionStart, IComLTxEvents::OnLtxTransactionStart, OnLtxTransactionStart, OnLtxTransactionStart method [COM+], OnLtxTransactionStart method [COM+],IComLTxEvents interface, comsvcs/IComLTxEvents::OnLtxTransactionStart, cos.icomltxevents_onltxtransactionstart
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
 - IComLTxEvents::OnLtxTransactionStart
 - comsvcs/IComLTxEvents::OnLtxTransactionStart
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
 - IComLTxEvents.OnLtxTransactionStart
---

# IComLTxEvents::OnLtxTransactionStart


## -description

Generated when a transaction is started.

The event ID for this event is EID_LTXSTART.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>