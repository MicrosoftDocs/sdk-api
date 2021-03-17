---
UID: NF:oaidl.ITypeInfo2.GetFuncCustData
title: ITypeInfo2::GetFuncCustData (oaidl.h)
description: Gets the custom data from the specified function.
helpviewer_keywords: ["GetFuncCustData","GetFuncCustData method [Automation]","GetFuncCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetFuncCustData method","ITypeInfo2.GetFuncCustData","ITypeInfo2::GetFuncCustData","_oa96_ITypeInfo2_GetFuncCustData","automat.itypeinfo2_getfunccustdata","oaidl/ITypeInfo2::GetFuncCustData"]
old-location: automat\itypeinfo2_getfunccustdata.htm
tech.root: automat
ms.assetid: d3a7b13f-6296-45ee-9697-4d52b5965c4b
ms.date: 12/05/2018
ms.keywords: GetFuncCustData, GetFuncCustData method [Automation], GetFuncCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetFuncCustData method, ITypeInfo2.GetFuncCustData, ITypeInfo2::GetFuncCustData, _oa96_ITypeInfo2_GetFuncCustData, automat.itypeinfo2_getfunccustdata, oaidl/ITypeInfo2::GetFuncCustData
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
 - ITypeInfo2::GetFuncCustData
 - oaidl/ITypeInfo2::GetFuncCustData
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
 - ITypeInfo2.GetFuncCustData
---

# ITypeInfo2::GetFuncCustData


## -description

Gets the custom data from the specified function.

## -parameters

### -param index [in]

The index of the function for which to get the custom data.

### -param guid [in]

The GUID used to identify the data.

### -param pVarVal [out]

The custom data.

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