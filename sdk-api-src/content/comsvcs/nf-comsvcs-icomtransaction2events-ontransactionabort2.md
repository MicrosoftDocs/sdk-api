---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionAbort2
title: IComTransaction2Events::OnTransactionAbort2 (comsvcs.h)
description: Generated when a transaction aborts. (IComTransaction2Events.OnTransactionAbort2)
helpviewer_keywords: ["IComTransaction2Events interface [COM+]","OnTransactionAbort2 method","IComTransaction2Events.OnTransactionAbort2","IComTransaction2Events::OnTransactionAbort2","OnTransactionAbort2","OnTransactionAbort2 method [COM+]","OnTransactionAbort2 method [COM+]","IComTransaction2Events interface","_dtc_icomtransaction2events_ontransactionabort2","comsvcs/IComTransaction2Events::OnTransactionAbort2","cos.icomtransaction2events_ontransactionabort2"]
old-location: cos\icomtransaction2events_ontransactionabort2.htm
tech.root: cos
ms.assetid: 8c74410c-c9a0-4115-876b-4b4db798e54f
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionAbort2 method, IComTransaction2Events.OnTransactionAbort2, IComTransaction2Events::OnTransactionAbort2, OnTransactionAbort2, OnTransactionAbort2 method [COM+], OnTransactionAbort2 method [COM+],IComTransaction2Events interface, _dtc_icomtransaction2events_ontransactionabort2, comsvcs/IComTransaction2Events::OnTransactionAbort2, cos.icomtransaction2events_ontransactionabort2
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
 - IComTransaction2Events::OnTransactionAbort2
 - comsvcs/IComTransaction2Events::OnTransactionAbort2
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
 - IComTransaction2Events.OnTransactionAbort2
---

# IComTransaction2Events::OnTransactionAbort2


## -description

Generated when a transaction aborts.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>
