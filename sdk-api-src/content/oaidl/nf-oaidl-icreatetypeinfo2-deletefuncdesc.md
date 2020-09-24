---
UID: NF:oaidl.ICreateTypeInfo2.DeleteFuncDesc
title: ICreateTypeInfo2::DeleteFuncDesc (oaidl.h)
description: Deletes a function description specified by the index number.
helpviewer_keywords: ["DeleteFuncDesc","DeleteFuncDesc method [Automation]","DeleteFuncDesc method [Automation]","ICreateTypeInfo2 interface","ICreateTypeInfo2 interface [Automation]","DeleteFuncDesc method","ICreateTypeInfo2.DeleteFuncDesc","ICreateTypeInfo2::DeleteFuncDesc","_oa96_ICreateTypeInfo2_DeleteFuncDesc","automat.icreatetypeinfo2_deletefuncdesc","oaidl/ICreateTypeInfo2::DeleteFuncDesc"]
old-location: automat\icreatetypeinfo2_deletefuncdesc.htm
tech.root: automat
ms.assetid: 5e157287-e4f3-49c4-9c18-a7b3ba1a965d
ms.date: 12/05/2018
ms.keywords: DeleteFuncDesc, DeleteFuncDesc method [Automation], DeleteFuncDesc method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteFuncDesc method, ICreateTypeInfo2.DeleteFuncDesc, ICreateTypeInfo2::DeleteFuncDesc, _oa96_ICreateTypeInfo2_DeleteFuncDesc, automat.icreatetypeinfo2_deletefuncdesc, oaidl/ICreateTypeInfo2::DeleteFuncDesc
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
 - ICreateTypeInfo2::DeleteFuncDesc
 - oaidl/ICreateTypeInfo2::DeleteFuncDesc
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
 - ICreateTypeInfo2.DeleteFuncDesc
---

# ICreateTypeInfo2::DeleteFuncDesc


## -description

Deletes a function description specified by the index number.

## -parameters

### -param index [in]

The index of the function whose description is to be deleted. The index should be in the range of 0 to 1 less than the number of functions in this type.

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