---
UID: NF:comsvcs.ITransactionProxy.Abort
title: ITransactionProxy::Abort (comsvcs.h)
description: Aborts the transaction.helpviewer_keywords: ["Abort","Abort method [COM+]","Abort method [COM+]","ITransactionProxy interface","ITransactionProxy interface [COM+]","Abort method","ITransactionProxy.Abort","ITransactionProxy::Abort","comsvcs/ITransactionProxy::Abort","cos.itransactionproxy_abort"]
old-location: cos\itransactionproxy_abort.htm
tech.root: cossdk
ms.assetid: 15ad94ac-311f-486d-988b-9071396f6e34
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [COM+], Abort method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],Abort method, ITransactionProxy.Abort, ITransactionProxy::Abort, comsvcs/ITransactionProxy::Abort, cos.itransactionproxy_abort
f1_keywords:
- comsvcs/ITransactionProxy.Abort
dev_langs:
- c++
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
- ITransactionProxy.Abort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransactionProxy::Abort


## -description


Aborts the transaction.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



Calling <b>ITransactionProxy::Abort</b> ends the transaction on return of the method and automatically deactivates all participating objects. Each resource manager enlisted in the transaction rolls back the operations performed on behalf of those objects.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>
 

 

