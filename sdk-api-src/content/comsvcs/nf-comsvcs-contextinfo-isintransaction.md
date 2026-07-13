---
UID: NF:comsvcs.ContextInfo.IsInTransaction
title: ContextInfo::IsInTransaction (comsvcs.h)
description: Indicates whether the current object is executing in a transaction. (ContextInfo.IsInTransaction)
helpviewer_keywords: ["ContextInfo interface [COM+]","IsInTransaction method","ContextInfo.IsInTransaction","ContextInfo::IsInTransaction","IsInTransaction","IsInTransaction method [COM+]","IsInTransaction method [COM+]","ContextInfo interface","_cos_ContextInfo_IsInTransaction","comsvcs/ContextInfo::IsInTransaction","cos.contextinfo_isintransaction"]
old-location: cos\contextinfo_isintransaction.htm
tech.root: cos
ms.assetid: 587805a4-6713-40be-83b6-5c772b5396cf
ms.date: 12/05/2018
ms.keywords: ContextInfo interface [COM+],IsInTransaction method, ContextInfo.IsInTransaction, ContextInfo::IsInTransaction, IsInTransaction, IsInTransaction method [COM+], IsInTransaction method [COM+],ContextInfo interface, _cos_ContextInfo_IsInTransaction, comsvcs/ContextInfo::IsInTransaction, cos.contextinfo_isintransaction
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
 - ContextInfo::IsInTransaction
 - comsvcs/ContextInfo::IsInTransaction
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
 - ContextInfo.IsInTransaction
---

# ContextInfo::IsInTransaction


## -description

Indicates whether the current object is executing in a transaction.

## -parameters

### -param pbIsInTx [out]

<b>TRUE</b> if the current object is executing within a transaction and <b>FALSE</b> otherwise.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>
