---
UID: NF:oaidl.ITypeInfo2.GetVarCustData
title: ITypeInfo2::GetVarCustData (oaidl.h)
description: Gets the custom data of the specified variable.
helpviewer_keywords: ["GetVarCustData","GetVarCustData method [Automation]","GetVarCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetVarCustData method","ITypeInfo2.GetVarCustData","ITypeInfo2::GetVarCustData","_oa96_ITypeInfo2_GetVarCustData","automat.itypeinfo2_getvarcustdata","oaidl/ITypeInfo2::GetVarCustData"]
old-location: automat\itypeinfo2_getvarcustdata.htm
tech.root: automat
ms.assetid: fe033b80-427d-48d1-99c8-4aba8909897e
ms.date: 12/05/2018
ms.keywords: GetVarCustData, GetVarCustData method [Automation], GetVarCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetVarCustData method, ITypeInfo2.GetVarCustData, ITypeInfo2::GetVarCustData, _oa96_ITypeInfo2_GetVarCustData, automat.itypeinfo2_getvarcustdata, oaidl/ITypeInfo2::GetVarCustData
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
 - ITypeInfo2::GetVarCustData
 - oaidl/ITypeInfo2::GetVarCustData
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
 - ITypeInfo2.GetVarCustData
---

# ITypeInfo2::GetVarCustData


## -description

Gets the custom data of the specified variable.

## -parameters

### -param index [in]

The index of the variable for which to get the custom data.

### -param guid [in]

The GUID used to identify the data.

### -param pVarVal [out]

The retrieved data.

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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>