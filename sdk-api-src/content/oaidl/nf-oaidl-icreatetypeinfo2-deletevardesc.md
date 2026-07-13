---
UID: NF:oaidl.ICreateTypeInfo2.DeleteVarDesc
title: ICreateTypeInfo2::DeleteVarDesc (oaidl.h)
description: Deletes the specified VARDESC structure. (ICreateTypeInfo2.DeleteVarDesc)
helpviewer_keywords: ["DeleteVarDesc","DeleteVarDesc method [Automation]","DeleteVarDesc method [Automation]","ICreateTypeInfo2 interface","ICreateTypeInfo2 interface [Automation]","DeleteVarDesc method","ICreateTypeInfo2.DeleteVarDesc","ICreateTypeInfo2::DeleteVarDesc","_oa96_ICreateTypeInfo2_DeleteVarDesc","automat.icreatetypeinfo2_deletevardesc","oaidl/ICreateTypeInfo2::DeleteVarDesc"]
old-location: automat\icreatetypeinfo2_deletevardesc.htm
tech.root: automat
ms.assetid: 0fcf55d9-2592-4fed-9612-48085eb7791b
ms.date: 12/05/2018
ms.keywords: DeleteVarDesc, DeleteVarDesc method [Automation], DeleteVarDesc method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteVarDesc method, ICreateTypeInfo2.DeleteVarDesc, ICreateTypeInfo2::DeleteVarDesc, _oa96_ICreateTypeInfo2_DeleteVarDesc, automat.icreatetypeinfo2_deletevardesc, oaidl/ICreateTypeInfo2::DeleteVarDesc
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
 - ICreateTypeInfo2::DeleteVarDesc
 - oaidl/ICreateTypeInfo2::DeleteVarDesc
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
 - ICreateTypeInfo2.DeleteVarDesc
---

# ICreateTypeInfo2::DeleteVarDesc


## -description

Deletes the specified VARDESC structure.

## -parameters

### -param index [in]

The index number of the VARDESC structure.

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
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_IOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function cannot read from the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVDATAREAD</b></dt>
</dl>
</td>
<td width="60%">
The function cannot read from the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_UNSUPFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The type library has an old format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The type library cannot be opened.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a>
