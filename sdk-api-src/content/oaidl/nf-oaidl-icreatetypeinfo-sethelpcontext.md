---
UID: NF:oaidl.ICreateTypeInfo.SetHelpContext
title: ICreateTypeInfo::SetHelpContext (oaidl.h)
description: Sets the Help context ID of the type information.
helpviewer_keywords: ["ICreateTypeInfo interface [Automation]","SetHelpContext method","ICreateTypeInfo.SetHelpContext","ICreateTypeInfo::SetHelpContext","SetHelpContext","SetHelpContext method [Automation]","SetHelpContext method [Automation]","ICreateTypeInfo interface","_oa96_ICreateTypeInfo_SetHelpContext","automat.icreatetypeinfo_sethelpcontext","oaidl/ICreateTypeInfo::SetHelpContext"]
old-location: automat\icreatetypeinfo_sethelpcontext.htm
tech.root: automat
ms.assetid: 8f61500a-29b5-48e4-b8ee-584cf5430274
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo interface [Automation],SetHelpContext method, ICreateTypeInfo.SetHelpContext, ICreateTypeInfo::SetHelpContext, SetHelpContext, SetHelpContext method [Automation], SetHelpContext method [Automation],ICreateTypeInfo interface, _oa96_ICreateTypeInfo_SetHelpContext, automat.icreatetypeinfo_sethelpcontext, oaidl/ICreateTypeInfo::SetHelpContext
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
 - ICreateTypeInfo::SetHelpContext
 - oaidl/ICreateTypeInfo::SetHelpContext
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
 - ICreateTypeInfo.SetHelpContext
---

# ICreateTypeInfo::SetHelpContext


## -description

Sets the Help context ID of the type information.

## -parameters

### -param dwHelpContext [in]

A handle to the Help context.

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