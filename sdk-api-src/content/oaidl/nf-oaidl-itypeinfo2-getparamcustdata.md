---
UID: NF:oaidl.ITypeInfo2.GetParamCustData
title: ITypeInfo2::GetParamCustData (oaidl.h)
description: Gets the custom data of the specified parameter.
helpviewer_keywords: ["GetParamCustData","GetParamCustData method [Automation]","GetParamCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetParamCustData method","ITypeInfo2.GetParamCustData","ITypeInfo2::GetParamCustData","_oa96_ITypeInfo2_GetParamCustData","automat.itypeinfo2_getparamcustdata","oaidl/ITypeInfo2::GetParamCustData"]
old-location: automat\itypeinfo2_getparamcustdata.htm
tech.root: automat
ms.assetid: 9342c364-58bb-47fa-b2c0-aae7df1ccdb5
ms.date: 12/05/2018
ms.keywords: GetParamCustData, GetParamCustData method [Automation], GetParamCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetParamCustData method, ITypeInfo2.GetParamCustData, ITypeInfo2::GetParamCustData, _oa96_ITypeInfo2_GetParamCustData, automat.itypeinfo2_getparamcustdata, oaidl/ITypeInfo2::GetParamCustData
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
 - ITypeInfo2::GetParamCustData
 - oaidl/ITypeInfo2::GetParamCustData
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
 - ITypeInfo2.GetParamCustData
---

# ITypeInfo2::GetParamCustData


## -description

Gets the custom data of the specified parameter.

## -parameters

### -param indexFunc [in]

The index of the function for which to get the custom data.

### -param indexParam [in]

The index of the parameter of this function for which to get the custom data.

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