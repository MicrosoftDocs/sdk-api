---
UID: NF:oaidl.ICreateTypeLib.CreateTypeInfo
title: ICreateTypeLib::CreateTypeInfo (oaidl.h)
description: Creates a new type description instance within the type library.
helpviewer_keywords: ["CreateTypeInfo","CreateTypeInfo method [Automation]","CreateTypeInfo method [Automation]","ICreateTypeLib interface","ICreateTypeLib interface [Automation]","CreateTypeInfo method","ICreateTypeLib.CreateTypeInfo","ICreateTypeLib::CreateTypeInfo","_oa96_ICreateTypeLib_CreateTypeInfo","automat.icreatetypelib_createtypeinfo","oaidl/ICreateTypeLib::CreateTypeInfo"]
old-location: automat\icreatetypelib_createtypeinfo.htm
tech.root: automat
ms.assetid: 5e9678af-661b-4033-bd3f-607c064f4245
ms.date: 12/05/2018
ms.keywords: CreateTypeInfo, CreateTypeInfo method [Automation], CreateTypeInfo method [Automation],ICreateTypeLib interface, ICreateTypeLib interface [Automation],CreateTypeInfo method, ICreateTypeLib.CreateTypeInfo, ICreateTypeLib::CreateTypeInfo, _oa96_ICreateTypeLib_CreateTypeInfo, automat.icreatetypelib_createtypeinfo, oaidl/ICreateTypeLib::CreateTypeInfo
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
 - ICreateTypeLib::CreateTypeInfo
 - oaidl/ICreateTypeLib::CreateTypeInfo
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
 - ICreateTypeLib.CreateTypeInfo
---

# ICreateTypeLib::CreateTypeInfo


## -description

Creates a new type description instance within the type library.

## -parameters

### -param szName [in]

The name of the new type.

### -param tkind [in]

TYPEKIND of the type description to be created.

### -param ppCTInfo [out]

The type description.

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
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_NAMECONFLICT</b></dt>
</dl>
</td>
<td width="60%">
The provided name is not unique.


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

Use <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> to create a new type description instance within the library. An error is returned if the specified name already appears in the library. Valid <i>tkind</i> values are described in TYPEKIND. To get the type information of the type description that is being created, call <code>IUnknown::QueryInterface(IID_ITypeInfo, ...)</code> on the returned <b>ICreateTypeLib</b>. This type information can be used by other type descriptions that reference it by using <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreatetypeinfo-addreftypeinfo">ICreateTypeInfo::AddRefTypeInfo</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>