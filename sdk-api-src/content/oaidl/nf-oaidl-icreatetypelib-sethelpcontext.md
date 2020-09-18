---
UID: NF:oaidl.ICreateTypeLib.SetHelpContext
title: ICreateTypeLib::SetHelpContext (oaidl.h)
description: Sets the Help context ID for retrieving general Help information for the type library.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetHelpContext method","ICreateTypeLib.SetHelpContext","ICreateTypeLib::SetHelpContext","SetHelpContext","SetHelpContext method [Automation]","SetHelpContext method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetHelpContext","automat.icreatetypelib_sethelpcontext","oaidl/ICreateTypeLib::SetHelpContext"]
old-location: automat\icreatetypelib_sethelpcontext.htm
tech.root: automat
ms.assetid: 58d7cd77-cfb6-493e-a9fd-26f469eec9f0
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetHelpContext method, ICreateTypeLib.SetHelpContext, ICreateTypeLib::SetHelpContext, SetHelpContext, SetHelpContext method [Automation], SetHelpContext method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetHelpContext, automat.icreatetypelib_sethelpcontext, oaidl/ICreateTypeLib::SetHelpContext
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
 - ICreateTypeLib::SetHelpContext
 - oaidl/ICreateTypeLib::SetHelpContext
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
 - ICreateTypeLib.SetHelpContext
---

# ICreateTypeLib::SetHelpContext


## -description

Sets the Help context ID for retrieving general Help information for the type library.

## -parameters

### -param dwHelpContext [in]

The Help context ID.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>

## -remarks

Calling <b>SetHelpContext</b> with a Help context of zero is equivalent to not calling it at all, because zero indicates a null Help context.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>