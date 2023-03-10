---
UID: NF:comsvcs.ContextInfo.GetTransactionId
title: ContextInfo::GetTransactionId (comsvcs.h)
description: Retrieves the transaction identifier associated with the object context. Objects in the same transaction share the same transaction identifier.
helpviewer_keywords: ["ContextInfo interface [COM+]","GetTransactionId method","ContextInfo.GetTransactionId","ContextInfo::GetTransactionId","GetTransactionId","GetTransactionId method [COM+]","GetTransactionId method [COM+]","ContextInfo interface","_cos_ContextInfo_GetTransactionId","comsvcs/ContextInfo::GetTransactionId","cos.contextinfo_gettransactionid"]
old-location: cos\contextinfo_gettransactionid.htm
tech.root: cos
ms.assetid: 9eb77a13-14f0-4d45-a6de-4ae28d6bcac4
ms.date: 12/05/2018
ms.keywords: ContextInfo interface [COM+],GetTransactionId method, ContextInfo.GetTransactionId, ContextInfo::GetTransactionId, GetTransactionId, GetTransactionId method [COM+], GetTransactionId method [COM+],ContextInfo interface, _cos_ContextInfo_GetTransactionId, comsvcs/ContextInfo::GetTransactionId, cos.contextinfo_gettransactionid
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
 - ContextInfo::GetTransactionId
 - comsvcs/ContextInfo::GetTransactionId
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
 - ContextInfo.GetTransactionId
---

# ContextInfo::GetTransactionId


## -description

Retrieves the transaction identifier associated with the object context. Objects in the same transaction share the same transaction identifier.

## -parameters

### -param pbstrTxId [out]

A reference to the transaction identifier.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOTRANSACTION</b></dt>
</dl>
</td>
<td width="60%">
The object is not executing within a transaction.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>