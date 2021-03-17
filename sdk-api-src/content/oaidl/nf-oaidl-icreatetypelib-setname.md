---
UID: NF:oaidl.ICreateTypeLib.SetName
title: ICreateTypeLib::SetName (oaidl.h)
description: Sets the name of the type library.
helpviewer_keywords: ["ICreateTypeLib interface [Automation]","SetName method","ICreateTypeLib.SetName","ICreateTypeLib::SetName","SetName","SetName method [Automation]","SetName method [Automation]","ICreateTypeLib interface","_oa96_ICreateTypeLib_SetName","automat.icreatetypelib_setname","oaidl/ICreateTypeLib::SetName"]
old-location: automat\icreatetypelib_setname.htm
tech.root: automat
ms.assetid: b533d2a1-f008-4345-8545-aebe14aa44f5
ms.date: 12/05/2018
ms.keywords: ICreateTypeLib interface [Automation],SetName method, ICreateTypeLib.SetName, ICreateTypeLib::SetName, SetName, SetName method [Automation], SetName method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetName, automat.icreatetypelib_setname, oaidl/ICreateTypeLib::SetName
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
 - ICreateTypeLib::SetName
 - oaidl/ICreateTypeLib::SetName
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
 - ICreateTypeLib.SetName
---

# ICreateTypeLib::SetName


## -description

Sets the name of the type library.

## -parameters

### -param szName [in]

The name to be assigned to the library.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a>