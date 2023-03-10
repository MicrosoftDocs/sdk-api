---
UID: NF:oaidl.ICreateTypeInfo2.DeleteVarDescByMemId
title: ICreateTypeInfo2::DeleteVarDescByMemId (oaidl.h)
description: Deletes the specified VARDESC structure. (ICreateTypeInfo2.DeleteVarDescByMemId)
helpviewer_keywords: ["DeleteVarDescByMemId","DeleteVarDescByMemId method [Automation]","DeleteVarDescByMemId method [Automation]","ICreateTypeInfo2 interface","ICreateTypeInfo2 interface [Automation]","DeleteVarDescByMemId method","ICreateTypeInfo2.DeleteVarDescByMemId","ICreateTypeInfo2::DeleteVarDescByMemId","_oa96_ICreateTypeInfo2_DeleteVarDescByMemId","automat.icreatetypeinfo2_deletevardescbymemid","oaidl/ICreateTypeInfo2::DeleteVarDescByMemId"]
old-location: automat\icreatetypeinfo2_deletevardescbymemid.htm
tech.root: automat
ms.assetid: 5b69dda9-01b5-45b2-ab92-65a29a2d1f21
ms.date: 12/05/2018
ms.keywords: DeleteVarDescByMemId, DeleteVarDescByMemId method [Automation], DeleteVarDescByMemId method [Automation],ICreateTypeInfo2 interface, ICreateTypeInfo2 interface [Automation],DeleteVarDescByMemId method, ICreateTypeInfo2.DeleteVarDescByMemId, ICreateTypeInfo2::DeleteVarDescByMemId, _oa96_ICreateTypeInfo2_DeleteVarDescByMemId, automat.icreatetypeinfo2_deletevardescbymemid, oaidl/ICreateTypeInfo2::DeleteVarDescByMemId
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
 - ICreateTypeInfo2::DeleteVarDescByMemId
 - oaidl/ICreateTypeInfo2::DeleteVarDescByMemId
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
 - ICreateTypeInfo2.DeleteVarDescByMemId
---

# ICreateTypeInfo2::DeleteVarDescByMemId


## -description

Deletes the specified VARDESC structure.

## -parameters

### -param memid [in]

The member identifier of the VARDESC to be deleted.

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
