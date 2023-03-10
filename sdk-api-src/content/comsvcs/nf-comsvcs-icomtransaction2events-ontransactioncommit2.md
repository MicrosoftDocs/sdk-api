---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionCommit2
title: IComTransaction2Events::OnTransactionCommit2 (comsvcs.h)
description: Generated when a transaction commits. (IComTransaction2Events.OnTransactionCommit2)
helpviewer_keywords: ["IComTransaction2Events interface [COM+]","OnTransactionCommit2 method","IComTransaction2Events.OnTransactionCommit2","IComTransaction2Events::OnTransactionCommit2","OnTransactionCommit2","OnTransactionCommit2 method [COM+]","OnTransactionCommit2 method [COM+]","IComTransaction2Events interface","_dtc_icomtransaction2events_ontransactioncommit2","comsvcs/IComTransaction2Events::OnTransactionCommit2","cos.icomtransaction2events_ontransactioncommit2"]
old-location: cos\icomtransaction2events_ontransactioncommit2.htm
tech.root: cos
ms.assetid: e68ba7be-876b-446a-8f82-a6e7af503b2c
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionCommit2 method, IComTransaction2Events.OnTransactionCommit2, IComTransaction2Events::OnTransactionCommit2, OnTransactionCommit2, OnTransactionCommit2 method [COM+], OnTransactionCommit2 method [COM+],IComTransaction2Events interface, _dtc_icomtransaction2events_ontransactioncommit2, comsvcs/IComTransaction2Events::OnTransactionCommit2, cos.icomtransaction2events_ontransactioncommit2
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
 - IComTransaction2Events::OnTransactionCommit2
 - comsvcs/IComTransaction2Events::OnTransactionCommit2
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
 - IComTransaction2Events.OnTransactionCommit2
---

# IComTransaction2Events::OnTransactionCommit2


## -description

Generated when a transaction commits.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>
