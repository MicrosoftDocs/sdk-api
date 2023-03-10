---
UID: NF:oaidl.ICreateTypeInfo.AddVarDesc
title: ICreateTypeInfo::AddVarDesc (oaidl.h)
description: Adds a variable or data member description to the type description.
helpviewer_keywords: ["AddVarDesc","AddVarDesc method [Automation]","AddVarDesc method [Automation]","ICreateTypeInfo interface","ICreateTypeInfo interface [Automation]","AddVarDesc method","ICreateTypeInfo.AddVarDesc","ICreateTypeInfo::AddVarDesc","_oa96_ICreateTypeInfo_AddVarDesc","automat.icreatetypeinfo_addvardesc","oaidl/ICreateTypeInfo::AddVarDesc"]
old-location: automat\icreatetypeinfo_addvardesc.htm
tech.root: automat
ms.assetid: db576528-fefc-4a22-bc24-d5ea037eae26
ms.date: 12/05/2018
ms.keywords: AddVarDesc, AddVarDesc method [Automation], AddVarDesc method [Automation],ICreateTypeInfo interface, ICreateTypeInfo interface [Automation],AddVarDesc method, ICreateTypeInfo.AddVarDesc, ICreateTypeInfo::AddVarDesc, _oa96_ICreateTypeInfo_AddVarDesc, automat.icreatetypeinfo_addvardesc, oaidl/ICreateTypeInfo::AddVarDesc
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
 - ICreateTypeInfo::AddVarDesc
 - oaidl/ICreateTypeInfo::AddVarDesc
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
 - ICreateTypeInfo.AddVarDesc
---

# ICreateTypeInfo::AddVarDesc


## -description

Adds a variable or data member description to the type description.

## -parameters

### -param index [in]

The index of the variable or data member to be added to the type description.

### -param pVarDesc [in]

A pointer to the variable or data member description to be added.

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

The index specifies the order of the variables. The first variable has an index of zero. <b>ICreateTypeInfo::AddVarDesc</b> returns an error if the specified index is greater than the number of variables currently in the type information. Calling this function does not pass ownership of the VARDESC structure to <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>. The instance field (oInst) of the VARDESC structure is ignored. This attribute is set only when <a href="/previous-versions/windows/desktop/automat/out">ICreateTypeInfo::LayOut</a> is called. Also, the member ID fields within the VARDESCs are ignored unless the TYPEKIND of the class is TKIND_DISPATCH.

Any HREFTYPE fields in the VARDESC structure must have been produced by the same instance of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> for which <b>AddVarDesc</b> is called.



<b>AddVarDesc</b> ignores the contents of the idldesc field of the ELEMDESC.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>