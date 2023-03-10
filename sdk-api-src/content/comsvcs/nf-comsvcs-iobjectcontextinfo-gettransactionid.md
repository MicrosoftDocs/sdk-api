---
UID: NF:comsvcs.IObjectContextInfo.GetTransactionId
title: IObjectContextInfo::GetTransactionId (comsvcs.h)
description: Retrieves the identifier of the current transaction.
helpviewer_keywords: ["GetTransactionId","GetTransactionId method [COM+]","GetTransactionId method [COM+]","IObjectContextInfo interface","IObjectContextInfo interface [COM+]","GetTransactionId method","IObjectContextInfo.GetTransactionId","IObjectContextInfo::GetTransactionId","_cos_IObjectContextInfo_GetTransactionId","comsvcs/IObjectContextInfo::GetTransactionId","cos.iobjectcontextinfo_gettransactionid"]
old-location: cos\iobjectcontextinfo_gettransactionid.htm
tech.root: cos
ms.assetid: c8aa6fe8-acb2-4e00-a7fc-605bb56969e6
ms.date: 12/05/2018
ms.keywords: GetTransactionId, GetTransactionId method [COM+], GetTransactionId method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetTransactionId method, IObjectContextInfo.GetTransactionId, IObjectContextInfo::GetTransactionId, _cos_IObjectContextInfo_GetTransactionId, comsvcs/IObjectContextInfo::GetTransactionId, cos.iobjectcontextinfo_gettransactionid
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
 - IObjectContextInfo::GetTransactionId
 - comsvcs/IObjectContextInfo::GetTransactionId
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
 - IObjectContextInfo.GetTransactionId
---

# IObjectContextInfo::GetTransactionId


## -description

Retrieves the identifier of the current transaction.

## -parameters

### -param pGuid [out]

A GUID that identifies the current transaction.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not executing in a transaction.

</td>
</tr>
</table>

## -remarks

Objects in the same transaction share the same transaction identifier.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>