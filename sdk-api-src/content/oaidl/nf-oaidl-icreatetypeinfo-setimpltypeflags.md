---
UID: NF:oaidl.ICreateTypeInfo.SetImplTypeFlags
title: ICreateTypeInfo::SetImplTypeFlags (oaidl.h)
description: Sets the attributes for an implemented or inherited interface of a type.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetImplTypeFlags method","ICreateTypeInfo.SetImplTypeFlags","ICreateTypeInfo::SetImplTypeFlags","SetImplTypeFlags","SetImplTypeFlags method [Automation]","SetImplTypeFlags method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetImplTypeFlags","automat.icreatetypeinfo_setimpltypeflags","oaidl/ICreateTypeInfo::SetImplTypeFlags"]
old-location: automat\icreatetypeinfo_setimpltypeflags.htm
tech.root: automat
ms.assetid: 712b7d02-0181-4a21-9221-514c062af171
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetImplTypeFlags method, ICreateTypeInfo.SetImplTypeFlags, ICreateTypeInfo::SetImplTypeFlags, SetImplTypeFlags, SetImplTypeFlags method [Automation], SetImplTypeFlags method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetImplTypeFlags, automat.icreatetypeinfo_setimpltypeflags, oaidl/ICreateTypeInfo::SetImplTypeFlags
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
 - ICreateTypeInfo::SetImplTypeFlags
 - oaidl/ICreateTypeInfo::SetImplTypeFlags
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
 - ICreateTypeInfo.SetImplTypeFlags
---

# ICreateTypeInfo::SetImplTypeFlags


## -description

Sets the attributes for an implemented or inherited interface of a type.

## -parameters

### -param index [in]

The index of the interface for which to set type flags.

### -param implTypeFlags [in]

IMPLTYPE flags to be set.

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