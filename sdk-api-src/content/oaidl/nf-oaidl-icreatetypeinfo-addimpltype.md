---
UID: NF:oaidl.ICreateTypeInfo.AddImplType
title: ICreateTypeInfo::AddImplType (oaidl.h)
description: Specifies an inherited interface, or an interface implemented by a component object class (coclass).
helpviewer_keywords: ["AddImplType","AddImplType method [Automation]","AddImplType method [Automation]","ICreateTypeInfo interface","ICreateTypeInfo interface [Automation]","AddImplType method","ICreateTypeInfo.AddImplType","ICreateTypeInfo::AddImplType","_oa96_ICreateTypeInfo_AddImplType","automat.icreatetypeinfo_addimpltype","oaidl/ICreateTypeInfo::AddImplType"]
old-location: automat\icreatetypeinfo_addimpltype.htm
tech.root: automat
ms.assetid: fef8421f-67de-402b-8efd-7a104c84ca6e
ms.date: 12/05/2018
ms.keywords: AddImplType, AddImplType method [Automation], AddImplType method [Automation],ICreateTypeInfo interface, ICreateTypeInfo interface [Automation],AddImplType method, ICreateTypeInfo.AddImplType, ICreateTypeInfo::AddImplType, _oa96_ICreateTypeInfo_AddImplType, automat.icreatetypeinfo_addimpltype, oaidl/ICreateTypeInfo::AddImplType
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
 - ICreateTypeInfo::AddImplType
 - oaidl/ICreateTypeInfo::AddImplType
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
 - ICreateTypeInfo.AddImplType
---

# ICreateTypeInfo::AddImplType


## -description

Specifies an inherited interface, or an interface implemented by a component object class (coclass).

## -parameters

### -param index [in]

The index of the implementation class to be added. Specifies the order of the type relative to the other type.

### -param hRefType [in]

A handle to the referenced type description obtained from the <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addreftypeinfo">AddRefType</a> description.

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

To specify an inherited interface, use index = 0. For a dispinterface with Syntax 2, call <b>ICreateTypeInfo::AddImplType</b> twice, once with <i>index</i> = 0 for the inherited <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and once with <i>index</i> = 1 for the interface that is being wrapped. For a dual interface, call <b>ICreateTypeInfo::AddImplType</b> with <i>index</i> = -1 for the TKIND_INTERFACE type information component of the dual interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>