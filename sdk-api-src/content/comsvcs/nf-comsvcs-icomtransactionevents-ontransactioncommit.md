---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionCommit
title: IComTransactionEvents::OnTransactionCommit (comsvcs.h)
description: Generated when a transaction commits. (IComTransactionEvents.OnTransactionCommit)
helpviewer_keywords: ["IComTransactionEvents interface [COM+]","OnTransactionCommit method","IComTransactionEvents.OnTransactionCommit","IComTransactionEvents::OnTransactionCommit","OnTransactionCommit","OnTransactionCommit method [COM+]","OnTransactionCommit method [COM+]","IComTransactionEvents interface","_dtc_IComTransactionEvents_OnTransactionCommit","comsvcs/IComTransactionEvents::OnTransactionCommit","cos.icomtransactionevents_ontransactioncommit"]
old-location: cos\icomtransactionevents_ontransactioncommit.htm
tech.root: cos
ms.assetid: c86b8b07-3dd0-48b8-9119-cb438238fc50
ms.date: 12/05/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionCommit method, IComTransactionEvents.OnTransactionCommit, IComTransactionEvents::OnTransactionCommit, OnTransactionCommit, OnTransactionCommit method [COM+], OnTransactionCommit method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionCommit, comsvcs/IComTransactionEvents::OnTransactionCommit, cos.icomtransactionevents_ontransactioncommit
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
 - IComTransactionEvents::OnTransactionCommit
 - comsvcs/IComTransactionEvents::OnTransactionCommit
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
 - IComTransactionEvents.OnTransactionCommit
---

# IComTransactionEvents::OnTransactionCommit


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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransactionevents">IComTransactionEvents</a>
