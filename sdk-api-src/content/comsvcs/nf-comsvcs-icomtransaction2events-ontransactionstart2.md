---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionStart2
title: IComTransaction2Events::OnTransactionStart2 (comsvcs.h)
description: Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts. (IComTransaction2Events.OnTransactionStart2)
helpviewer_keywords: ["IComTransaction2Events interface [COM+]","OnTransactionStart2 method","IComTransaction2Events.OnTransactionStart2","IComTransaction2Events::OnTransactionStart2","OnTransactionStart2","OnTransactionStart2 method [COM+]","OnTransactionStart2 method [COM+]","IComTransaction2Events interface","_dtc_icomtransaction2events_ontransactionstart2","comsvcs/IComTransaction2Events::OnTransactionStart2","cos.icomtransaction2events_ontransactionstart2"]
old-location: cos\icomtransaction2events_ontransactionstart2.htm
tech.root: cos
ms.assetid: c7666b9f-5485-47da-9027-25668e73f73b
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionStart2 method, IComTransaction2Events.OnTransactionStart2, IComTransaction2Events::OnTransactionStart2, OnTransactionStart2, OnTransactionStart2 method [COM+], OnTransactionStart2 method [COM+],IComTransaction2Events interface, _dtc_icomtransaction2events_ontransactionstart2, comsvcs/IComTransaction2Events::OnTransactionStart2, cos.icomtransaction2events_ontransactionstart2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComTransaction2Events::OnTransactionStart2
 - comsvcs/IComTransaction2Events::OnTransactionStart2
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
 - IComTransaction2Events.OnTransactionStart2
---

# IComTransaction2Events::OnTransactionStart2


## -description

Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

### -param tsid [in]

The transaction stream identifier for the correlation to objects.

### -param fRoot [in]

Indicates whether the transaction is a root transaction.

### -param nIsolationLevel [in]

The isolation level of the transaction.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>
