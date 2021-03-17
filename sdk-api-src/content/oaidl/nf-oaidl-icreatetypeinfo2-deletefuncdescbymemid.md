---
UID: NF:oaidl.ICreateTypeInfo2.DeleteFuncDescByMemId
title: ICreateTypeInfo2::DeleteFuncDescByMemId (oaidl.h)
description: Deletes the specified function description (FUNCDESC).
helpviewer_keywords: ["DeleteFuncDescByMemId","DeleteFuncDescByMemId method [Automation]","DeleteFuncDescByMemId method [Automation]","ICreateTypeInfo2 interface","ICreateTypeInfo2 interface [Automation]","DeleteFuncDescByMemId method","ICreateTypeInfo2.DeleteFuncDescByMemId","ICreateTypeInfo2::DeleteFuncDescByMemId","_oa96_ICreateTypeInfo2_DeleteFuncDescByMemId","automat.icreatetypeinfo2_deletefuncdescbymemid","oaidl/ICreateTypeInfo2::DeleteFuncDescByMemId"]
old-location: automat\icreatetypeinfo2_deletefuncdescbymemid.htm
tech.root: automat
ms.assetid: 75de562b-3c08-4bab-957a-3a9eab16fb3f
ms.date: 12/05/2018
ms.keywords: DeleteFuncDescByMemId, DeleteFuncDescByMemId method [Automation], DeleteFuncDescByMemId method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteFuncDescByMemId method, ICreateTypeInfo2.DeleteFuncDescByMemId, ICreateTypeInfo2::DeleteFuncDescByMemId, _oa96_ICreateTypeInfo2_DeleteFuncDescByMemId, automat.icreatetypeinfo2_deletefuncdescbymemid, oaidl/ICreateTypeInfo2::DeleteFuncDescByMemId
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ICreateTypeInfo2::DeleteFuncDescByMemId
 - oaidl/ICreateTypeInfo2::DeleteFuncDescByMemId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeInfo2.DeleteFuncDescByMemId
---

# ICreateTypeInfo2::DeleteFuncDescByMemId


## -description

Deletes the specified function description (FUNCDESC).

## -parameters

### -param memid [in]

The member identifier of the FUNCDESC to delete.

### -param invKind [in]

The type of the invocation.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a>