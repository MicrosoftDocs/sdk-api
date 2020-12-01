---
UID: NF:oaidl.ICreateTypeInfo.AddRefTypeInfo
title: ICreateTypeInfo::AddRefTypeInfo (oaidl.h)
description: Adds a type description to those referenced by the type description being created.
helpviewer_keywords: ["AddRefTypeInfo","AddRefTypeInfo method [Automation]","AddRefTypeInfo method [Automation]","ICreateTypeInfo interface","ICreateTypeInfo interface [Automation]","AddRefTypeInfo method","ICreateTypeInfo.AddRefTypeInfo","ICreateTypeInfo::AddRefTypeInfo","_oa96_ICreateTypeInfo_AddRefTypeInfo","automat.icreatetypeinfo_addreftypeinfo","oaidl/ICreateTypeInfo::AddRefTypeInfo"]
old-location: automat\icreatetypeinfo_addreftypeinfo.htm
tech.root: automat
ms.assetid: cb7f41f1-81a6-406f-916f-d1d1a8c093b5
ms.date: 12/05/2018
ms.keywords: AddRefTypeInfo, AddRefTypeInfo method [Automation], AddRefTypeInfo method [Automation],ICreateTypeInfo interface, ICreateTypeInfo interface [Automation],AddRefTypeInfo method, ICreateTypeInfo.AddRefTypeInfo, ICreateTypeInfo::AddRefTypeInfo, _oa96_ICreateTypeInfo_AddRefTypeInfo, automat.icreatetypeinfo_addreftypeinfo, oaidl/ICreateTypeInfo::AddRefTypeInfo
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
 - ICreateTypeInfo::AddRefTypeInfo
 - oaidl/ICreateTypeInfo::AddRefTypeInfo
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
 - ICreateTypeInfo.AddRefTypeInfo
---

# ICreateTypeInfo::AddRefTypeInfo


## -description

Adds a type description to those referenced by the type description being created.

## -parameters

### -param pTInfo [in]

The type description to be referenced.

### -param phRefType [in]

The handle that this type description associates with the referenced type information.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot write to the destination.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY
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
<dt><b>TYPE_E_WRONGTYPEKIND</b></dt>
</dl>
</td>
<td width="60%">
Type mismatch.

</td>
</tr>
</table>

## -remarks

The second parameter returns a pointer to the handle of the added type information. If <b>AddRefTypeInfo</b> has been called previously for the same type information, the index that was returned by the previous call is returned in <i>phRefType</i>. If the referenced type description is in the type library being created, its type information can be obtained by calling IUnknown::QueryInterface(IID_ITypeInfo, ...) on the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a> interface of that type description.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>