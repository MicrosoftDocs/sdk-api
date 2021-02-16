---
UID: NF:oaidl.ICreateTypeInfo.SetMops
title: ICreateTypeInfo::SetMops (oaidl.h)
description: Sets the marshaling opcode string associated with the type description or the function.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetMops method","ICreateTypeInfo.SetMops","ICreateTypeInfo::SetMops","SetMops","SetMops method [Automation]","SetMops method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetMops","automat.icreatetypeinfo_setmops","oaidl/ICreateTypeInfo::SetMops"]
old-location: automat\icreatetypeinfo_setmops.htm
tech.root: automat
ms.assetid: e775c2f9-2886-4aa0-a30c-445f317d0e02
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetMops method, ICreateTypeInfo.SetMops, ICreateTypeInfo::SetMops, SetMops, SetMops method [Automation], SetMops method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetMops, automat.icreatetypeinfo_setmops, oaidl/ICreateTypeInfo::SetMops
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
 - ICreateTypeInfo::SetMops
 - oaidl/ICreateTypeInfo::SetMops
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
 - ICreateTypeInfo.SetMops
---

# ICreateTypeInfo::SetMops


## -description

Sets the marshaling opcode string associated with the type description or the function.

## -parameters

### -param index [in]

The index of the member for which to set the opcode string. If index is –1, sets the opcode string for the type description.

### -param bstrMops [in]

The marshaling opcode string.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>