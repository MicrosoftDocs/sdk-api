---
UID: NF:oaidl.ICreateTypeInfo2.SetVarCustData
title: ICreateTypeInfo2::SetVarCustData (oaidl.h)
description: Sets a value for custom data for the specified variable.
helpviewer_keywords: ["ICreateTypeInfo2 interface [Automation]","SetVarCustData method","ICreateTypeInfo2.SetVarCustData","ICreateTypeInfo2::SetVarCustData","SetVarCustData","SetVarCustData method [Automation]","SetVarCustData method [Automation]","ICreateTypeInfo2 interface","_oa96_ICreateTypeInfo2_SetVarCustData","automat.icreatetypeinfo2_setvarcustdata","oaidl/ICreateTypeInfo2::SetVarCustData"]
old-location: automat\icreatetypeinfo2_setvarcustdata.htm
tech.root: automat
ms.assetid: 7055ad6b-89d8-47d9-bdfa-26b323e53133
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetVarCustData method, ICreateTypeInfo2.SetVarCustData, ICreateTypeInfo2::SetVarCustData, SetVarCustData, SetVarCustData method [Automation], SetVarCustData method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetVarCustData, automat.icreatetypeinfo2_setvarcustdata, oaidl/ICreateTypeInfo2::SetVarCustData
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
 - ICreateTypeInfo2::SetVarCustData
 - oaidl/ICreateTypeInfo2::SetVarCustData
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
 - ICreateTypeInfo2.SetVarCustData
---

# ICreateTypeInfo2::SetVarCustData


## -description

Sets a value for custom data for the specified variable.

## -parameters

### -param index [in]

The index of the variable for which to set the custom data.

### -param guid [in]

The globally unique ID (GUID) used to identify the data.

### -param pVarVal [in]

The data to store (any variant except an object).

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a>