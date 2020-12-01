---
UID: NF:oaidl.ICreateTypeInfo.SetVarDocString
title: ICreateTypeInfo::SetVarDocString (oaidl.h)
description: Sets the documentation string for the variable with the specified index.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetVarDocString method","ICreateTypeInfo.SetVarDocString","ICreateTypeInfo::SetVarDocString","SetVarDocString","SetVarDocString method [Automation]","SetVarDocString method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetVarDocString","automat.icreatetypeinfo_setvardocstring","oaidl/ICreateTypeInfo::SetVarDocString"]
old-location: automat\icreatetypeinfo_setvardocstring.htm
tech.root: automat
ms.assetid: 6bea2b52-30d8-454c-ad96-f94417640ce5
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetVarDocString method, ICreateTypeInfo.SetVarDocString, ICreateTypeInfo::SetVarDocString, SetVarDocString, SetVarDocString method [Automation], SetVarDocString method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetVarDocString, automat.icreatetypeinfo_setvardocstring, oaidl/ICreateTypeInfo::SetVarDocString
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
 - ICreateTypeInfo::SetVarDocString
 - oaidl/ICreateTypeInfo::SetVarDocString
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
 - ICreateTypeInfo.SetVarDocString
---

# ICreateTypeInfo::SetVarDocString


## -description

Sets the documentation string for the variable with the specified index.

## -parameters

### -param index [in]

The index of the variable.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>