---
UID: NF:oaidl.ICreateTypeLib2.DeleteTypeInfo
title: ICreateTypeLib2::DeleteTypeInfo (oaidl.h)
description: Deletes a specified type information from the type library.
helpviewer_keywords: ["DeleteTypeInfo","DeleteTypeInfo method [Automation]","DeleteTypeInfo method [Automation]","ICreateTypeLib2 interface","ICreateTypeLib2 interface [Automation]","DeleteTypeInfo method","ICreateTypeLib2.DeleteTypeInfo","ICreateTypeLib2::DeleteTypeInfo","_oa96_ICreateTypeLib2_DeleteTypeInfo","automat.icreatetypelib2_deletetypeinfo","oaidl/ICreateTypeLib2::DeleteTypeInfo"]
old-location: automat\icreatetypelib2_deletetypeinfo.htm
tech.root: automat
ms.assetid: 0a233830-631b-4a6d-8fce-eb8f47714e9c
ms.date: 12/05/2018
ms.keywords: DeleteTypeInfo, DeleteTypeInfo method [Automation], DeleteTypeInfo method [Automation],ICreateTypeLib2 interface, ICreateTypeLib2 interface [Automation],DeleteTypeInfo method, ICreateTypeLib2.DeleteTypeInfo, ICreateTypeLib2::DeleteTypeInfo, _oa96_ICreateTypeLib2_DeleteTypeInfo, automat.icreatetypelib2_deletetypeinfo, oaidl/ICreateTypeLib2::DeleteTypeInfo
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
 - ICreateTypeLib2::DeleteTypeInfo
 - oaidl/ICreateTypeLib2::DeleteTypeInfo
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
 - ICreateTypeLib2.DeleteTypeInfo
---

# ICreateTypeLib2::DeleteTypeInfo


## -description

Deletes a specified type information from the type library.

## -parameters

### -param szName [in]

The name of the type information to remove.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib2">ICreateTypeLib2</a>