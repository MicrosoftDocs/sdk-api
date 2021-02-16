---
UID: NF:oaidl.ICreateTypeInfo.SetFuncHelpContext
title: ICreateTypeInfo::SetFuncHelpContext (oaidl.h)
description: Sets the Help context ID for the function with the specified index.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetFuncHelpContext method","ICreateTypeInfo.SetFuncHelpContext","ICreateTypeInfo::SetFuncHelpContext","SetFuncHelpContext","SetFuncHelpContext method [Automation]","SetFuncHelpContext method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetFuncHelpContext","automat.icreatetypeinfo_setfunchelpcontext","oaidl/ICreateTypeInfo::SetFuncHelpContext"]
old-location: automat\icreatetypeinfo_setfunchelpcontext.htm
tech.root: automat
ms.assetid: 945d2faa-f35d-488f-a0df-ace3fbb85971
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetFuncHelpContext method, ICreateTypeInfo.SetFuncHelpContext, ICreateTypeInfo::SetFuncHelpContext, SetFuncHelpContext, SetFuncHelpContext method [Automation], SetFuncHelpContext method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetFuncHelpContext, automat.icreatetypeinfo_setfunchelpcontext, oaidl/ICreateTypeInfo::SetFuncHelpContext
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
 - ICreateTypeInfo::SetFuncHelpContext
 - oaidl/ICreateTypeInfo::SetFuncHelpContext
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
 - ICreateTypeInfo.SetFuncHelpContext
---

# ICreateTypeInfo::SetFuncHelpContext


## -description

Sets the Help context ID for the function with the specified index.

## -parameters

### -param index [in]

The index of the function.

### -param dwHelpContext [in]

The Help context ID for the Help topic.

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

<b>SetFuncHelpContext</b> only needs to be set once for each property, because all property accessor functions are identified by one name.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>