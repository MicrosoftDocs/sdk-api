---
UID: NF:oaidl.ITypeLib.FindName
title: ITypeLib::FindName (oaidl.h)
description: Finds occurrences of a type description in a type library. This may be used to quickly verify that a name exists in a type library.
helpviewer_keywords: ["FindName","FindName method [Automation]","FindName method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","FindName method","ITypeLib.FindName","ITypeLib::FindName","_oa96_ITypeLib_FindName","automat.itypelib_findname","oaidl/ITypeLib::FindName"]
old-location: automat\itypelib_findname.htm
tech.root: automat
ms.assetid: 932014a8-3a35-487a-b035-788fc28dacc2
ms.date: 12/05/2018
ms.keywords: FindName, FindName method [Automation], FindName method [Automation],ITypeLib interface, ITypeLib interface [Automation],FindName method, ITypeLib.FindName, ITypeLib::FindName, _oa96_ITypeLib_FindName, automat.itypelib_findname, oaidl/ITypeLib::FindName
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
 - ITypeLib::FindName
 - oaidl/ITypeLib::FindName
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
 - ITypeLib.FindName
---

# ITypeLib::FindName


## -description

Finds occurrences of a type description in a type library. This may be used to quickly verify that a name exists in a type library.

## -parameters

### -param szNameBuf [in, out]

The name to search for.

### -param lHashVal [in]

A hash value to speed up the search, computed by the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-lhashvalofnamesys">LHashValOfNameSys</a> function. If <i>lHashVal</i> = 0, a value is computed.

### -param ppTInfo [out]

An array of pointers to the type descriptions that contain the name specified in <i>szNameBuf</i>. This parameter cannot be null.

### -param rgMemId [out]

An array of the found items; <i>rgMemId</i>[<i>i</i>] is the MEMBERID that indexes into the type description specified by <i>ppTInfo</i>[<i>i</i>]. This parameter cannot be null.

### -param pcFound [in, out]

On entry, indicates how many instances to look for. For example, *<i>pcFound</i> = 1 can be called to find the first occurrence. The search stops when one is found.

On exit, indicates the number of instances that were found. If the in and out values of *<i>pcFound</i> are identical, there may be more type descriptions that contain the name.

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

Passing *<i>pcFound</i> = <i>n</i> indicates that there is enough room in the <i>ppTInfo</i> and <i>rgMemId</i> arrays for <i>n</i> (<i>ptinfo</i>, <i>memid</i>) pairs. The function returns MEMBERID_NIL in <i>rgMemId</i>[<i>i</i>], if the name in <i>szNameBuf</i> is the name of the type information in <i>ppTInfo</i>[<i>i</i>].

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>