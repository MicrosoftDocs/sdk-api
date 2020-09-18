---
UID: NF:oaidl.ICreateTypeInfo2.SetCustData
title: ICreateTypeInfo2::SetCustData (oaidl.h)
description: Sets a value for custom data.
helpviewer_keywords: ["ICreateTypeInfo2 interface [Automation]","SetCustData method","ICreateTypeInfo2.SetCustData","ICreateTypeInfo2::SetCustData","SetCustData","SetCustData method [Automation]","SetCustData method [Automation]","ICreateTypeInfo2 interface","_oa96_ICreateTypeInfo2_SetCustData","automat.icreatetypeinfo2_setcustdata","oaidl/ICreateTypeInfo2::SetCustData"]
old-location: automat\icreatetypeinfo2_setcustdata.htm
tech.root: automat
ms.assetid: 52a947c8-2860-4803-9df2-7b71b8b8ef87
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetCustData method, ICreateTypeInfo2.SetCustData, ICreateTypeInfo2::SetCustData, SetCustData, SetCustData method [Automation], SetCustData method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetCustData, automat.icreatetypeinfo2_setcustdata, oaidl/ICreateTypeInfo2::SetCustData
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
 - ICreateTypeInfo2::SetCustData
 - oaidl/ICreateTypeInfo2::SetCustData
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
 - ICreateTypeInfo2.SetCustData
---

# ICreateTypeInfo2::SetCustData


## -description

Sets a value for custom data.

## -parameters

### -param guid [in]

The unique identifier that can be used to identify the data.

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