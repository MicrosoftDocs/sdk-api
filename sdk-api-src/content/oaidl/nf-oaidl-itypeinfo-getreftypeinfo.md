---
UID: NF:oaidl.ITypeInfo.GetRefTypeInfo
title: ITypeInfo::GetRefTypeInfo (oaidl.h)
description: If a type description references other type descriptions, it retrieves the referenced type descriptions.
helpviewer_keywords: ["GetRefTypeInfo","GetRefTypeInfo method [Automation]","GetRefTypeInfo method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetRefTypeInfo method","ITypeInfo.GetRefTypeInfo","ITypeInfo::GetRefTypeInfo","_oa96_ITypeInfo_GetRefTypeInfo","automat.itypeinfo_getreftypeinfo","oaidl/ITypeInfo::GetRefTypeInfo"]
old-location: automat\itypeinfo_getreftypeinfo.htm
tech.root: automat
ms.assetid: 61d3b31d-6591-4e55-9e82-5246a168be00
ms.date: 12/05/2018
ms.keywords: GetRefTypeInfo, GetRefTypeInfo method [Automation], GetRefTypeInfo method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetRefTypeInfo method, ITypeInfo.GetRefTypeInfo, ITypeInfo::GetRefTypeInfo, _oa96_ITypeInfo_GetRefTypeInfo, automat.itypeinfo_getreftypeinfo, oaidl/ITypeInfo::GetRefTypeInfo
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
 - ITypeInfo::GetRefTypeInfo
 - oaidl/ITypeInfo::GetRefTypeInfo
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
 - ITypeInfo.GetRefTypeInfo
---

# ITypeInfo::GetRefTypeInfo


## -description

If a type description references other type descriptions, it retrieves the referenced type descriptions.

## -parameters

### -param hRefType [in]

A handle to the referenced type description to return.

### -param ppTInfo [out]

The referenced type description.

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

On return, the second parameter contains a pointer to a pointer to a type description that is referenced by this type description. A type description must have a reference to each type description that occurs as the type of any of its variables, function parameters, or function return types. For example, if the type of a data member is a record type, the type description for that data member contains the <i>hRefType</i> of a referenced type description. To get a pointer to the type description, the reference is passed to <b>GetRefTypeInfo</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>