---
UID: NF:oaidl.ICreateTypeInfo.SetFuncDocString
title: ICreateTypeInfo::SetFuncDocString (oaidl.h)
description: Sets the documentation string for the function with the specified index.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetFuncDocString method","ICreateTypeInfo.SetFuncDocString","ICreateTypeInfo::SetFuncDocString","SetFuncDocString","SetFuncDocString method [Automation]","SetFuncDocString method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetFuncDocString","automat.icreatetypeinfo_setfuncdocstring","oaidl/ICreateTypeInfo::SetFuncDocString"]
old-location: automat\icreatetypeinfo_setfuncdocstring.htm
tech.root: automat
ms.assetid: e2377502-b26f-401f-82f1-d65f739a684f
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetFuncDocString method, ICreateTypeInfo.SetFuncDocString, ICreateTypeInfo::SetFuncDocString, SetFuncDocString, SetFuncDocString method [Automation], SetFuncDocString method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetFuncDocString, automat.icreatetypeinfo_setfuncdocstring, oaidl/ICreateTypeInfo::SetFuncDocString
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
 - ICreateTypeInfo::SetFuncDocString
 - oaidl/ICreateTypeInfo::SetFuncDocString
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
 - ICreateTypeInfo.SetFuncDocString
---

# ICreateTypeInfo::SetFuncDocString


## -description

Sets the documentation string for the function with the specified index.

## -parameters

### -param index [in]

The index of the function.

### -param szDocString [in]

The documentation string.

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
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The element cannot be found.


</td>
</tr>
</table>

## -remarks

The documentation string is a brief description of the function intended for use by tools such as type browsers. <b>SetFuncDocString</b> only needs to be used once for each property, because all property accessor functions are identified by one name.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>