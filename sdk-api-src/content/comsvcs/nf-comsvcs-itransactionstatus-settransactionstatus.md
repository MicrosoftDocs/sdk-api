---
UID: NF:comsvcs.ITransactionStatus.SetTransactionStatus
title: ITransactionStatus::SetTransactionStatus (comsvcs.h)
description: Sets the transaction status to either committed or aborted. Do not use this method. It is used only internally by COM+.
helpviewer_keywords: ["ITransactionStatus interface [COM+]","SetTransactionStatus method","ITransactionStatus.SetTransactionStatus","ITransactionStatus::SetTransactionStatus","SetTransactionStatus","SetTransactionStatus method [COM+]","SetTransactionStatus method [COM+]","ITransactionStatus interface","_cos_ITransactionStatus_SetTransactionStatus","comsvcs/ITransactionStatus::SetTransactionStatus","cos.itransactionstatus_settransactionstatus"]
old-location: cos\itransactionstatus_settransactionstatus.htm
tech.root: cos
ms.assetid: 0e69758a-8dc7-489c-8e78-ba35749beb01
ms.date: 12/05/2018
ms.keywords: ITransactionStatus interface [COM+],SetTransactionStatus method, ITransactionStatus.SetTransactionStatus, ITransactionStatus::SetTransactionStatus, SetTransactionStatus, SetTransactionStatus method [COM+], SetTransactionStatus method [COM+],ITransactionStatus interface, _cos_ITransactionStatus_SetTransactionStatus, comsvcs/ITransactionStatus::SetTransactionStatus, cos.itransactionstatus_settransactionstatus
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITransactionStatus::SetTransactionStatus
 - comsvcs/ITransactionStatus::SetTransactionStatus
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
 - ITransactionStatus.SetTransactionStatus
---

# ITransactionStatus::SetTransactionStatus


## -description

Sets the transaction status to either committed or aborted. Do not use this method. It is used only internally by COM+.

## -parameters

### -param hrStatus [in]

The status of the transaction.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionstatus">ITransactionStatus</a>