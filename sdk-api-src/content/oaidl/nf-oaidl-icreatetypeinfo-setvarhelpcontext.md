---
UID: NF:oaidl.ICreateTypeInfo.SetVarHelpContext
title: ICreateTypeInfo::SetVarHelpContext (oaidl.h)
description: Sets the Help context ID for the variable with the specified index.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetVarHelpContext method","ICreateTypeInfo.SetVarHelpContext","ICreateTypeInfo::SetVarHelpContext","SetVarHelpContext","SetVarHelpContext method [Automation]","SetVarHelpContext method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetVarHelpContext","automat.icreatetypeinfo_setvarhelpcontext","oaidl/ICreateTypeInfo::SetVarHelpContext"]
old-location: automat\icreatetypeinfo_setvarhelpcontext.htm
tech.root: automat
ms.assetid: ab15e7fc-63fa-433f-9191-c7087143a7c1
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetVarHelpContext method, ICreateTypeInfo.SetVarHelpContext, ICreateTypeInfo::SetVarHelpContext, SetVarHelpContext, SetVarHelpContext method [Automation], SetVarHelpContext method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetVarHelpContext, automat.icreatetypeinfo_setvarhelpcontext, oaidl/ICreateTypeInfo::SetVarHelpContext
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
 - ICreateTypeInfo::SetVarHelpContext
 - oaidl/ICreateTypeInfo::SetVarHelpContext
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
 - ICreateTypeInfo.SetVarHelpContext
---

# ICreateTypeInfo::SetVarHelpContext


## -description

Sets the Help context ID for the variable with the specified index.

## -parameters

### -param index [in]

The index of the variable.

### -param dwHelpContext [in]

The handle to the Help context ID for the Help topic on the variable.

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