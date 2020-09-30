---
UID: NF:oaidl.ICreateTypeInfo.SetVarName
title: ICreateTypeInfo::SetVarName (oaidl.h)
description: Sets the name of a variable.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetVarName method","ICreateTypeInfo.SetVarName","ICreateTypeInfo::SetVarName","SetVarName","SetVarName method [Automation]","SetVarName method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetVarName","automat.icreatetypeinfo_setvarname","oaidl/ICreateTypeInfo::SetVarName"]
old-location: automat\icreatetypeinfo_setvarname.htm
tech.root: automat
ms.assetid: 9f51fc2a-74cc-4aab-89b7-0237c14ff7f5
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetVarName method, ICreateTypeInfo.SetVarName, ICreateTypeInfo::SetVarName, SetVarName, SetVarName method [Automation], SetVarName method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetVarName, automat.icreatetypeinfo_setvarname, oaidl/ICreateTypeInfo::SetVarName
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
 - ICreateTypeInfo::SetVarName
 - oaidl/ICreateTypeInfo::SetVarName
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
 - ICreateTypeInfo.SetVarName
---

# ICreateTypeInfo::SetVarName


## -description

Sets the name of a variable.

## -parameters

### -param index [in]

The index of the variable.

### -param szName [in]

The name.

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