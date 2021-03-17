---
UID: NF:oaidl.ITypeInfo.GetNames
title: ITypeInfo::GetNames (oaidl.h)
description: Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID.
helpviewer_keywords: ["GetNames","GetNames method [Automation]","GetNames method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetNames method","ITypeInfo.GetNames","ITypeInfo::GetNames","_oa96_ITypeInfo_GetNames","automat.itypeinfo_getnames","oaidl/ITypeInfo::GetNames"]
old-location: automat\itypeinfo_getnames.htm
tech.root: automat
ms.assetid: ff318d92-9624-48aa-a0f9-8b8826121753
ms.date: 12/05/2018
ms.keywords: GetNames, GetNames method [Automation], GetNames method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetNames method, ITypeInfo.GetNames, ITypeInfo::GetNames, _oa96_ITypeInfo_GetNames, automat.itypeinfo_getnames, oaidl/ITypeInfo::GetNames
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
 - ITypeInfo::GetNames
 - oaidl/ITypeInfo::GetNames
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
 - ITypeInfo.GetNames
---

# ITypeInfo::GetNames


## -description

Retrieves the variable with the specified member ID or the name of the property or method and the parameters that correspond to the specified function ID.

## -parameters

### -param memid [in]

The ID of the member whose name (or names) is to be returned.

### -param rgBstrNames [out]

The caller-allocated array. On return, each of the elements contains the name (or names) associated with the member.

### -param cMaxNames [in]

The length of the passed-in <i>rgBstrNames</i> array.

### -param pcNames [out]

The number of names in the <i>rgBstrNames</i> array.

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

## -remarks

The caller must release the returned BSTR array.



If the member ID identifies a property that is implemented with property functions, the property name is returned. For property get functions, the names of the function and its parameters are always returned.



For property put and put reference functions, the right side of the assignment is unnamed. If <i>cMaxNames</i> is less than is required to return all of the names of the parameters of a function, then only the names of the first <i>cMaxNames</i> - 1 parameters are returned. The names of the parameters are returned in the array in the same order that they appear elsewhere in the interface (for example, the same order in the parameter array associated with the FUNCDESC enumeration).



If the type description inherits from another type description, this function is recursive to the base type description, if necessary, to find the item with the requested member ID.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>