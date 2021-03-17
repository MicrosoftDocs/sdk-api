---
UID: NF:oaidl.ICreateTypeInfo2.SetParamCustData
title: ICreateTypeInfo2::SetParamCustData (oaidl.h)
description: Sets a value for the custom data for the specified parameter.
helpviewer_keywords: ["ICreateTypeInfo2 interface [Automation]","SetParamCustData method","ICreateTypeInfo2.SetParamCustData","ICreateTypeInfo2::SetParamCustData","SetParamCustData","SetParamCustData method [Automation]","SetParamCustData method [Automation]","ICreateTypeInfo2 interface","_oa96_ICreateTypeInfo2_SetParamCustData","automat.icreatetypeinfo2_setparamcustdata","oaidl/ICreateTypeInfo2::SetParamCustData"]
old-location: automat\icreatetypeinfo2_setparamcustdata.htm
tech.root: automat
ms.assetid: df1a1ab0-c971-4d3e-ba63-45be66330027
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2 interface [Automation],SetParamCustData method, ICreateTypeInfo2.SetParamCustData, ICreateTypeInfo2::SetParamCustData, SetParamCustData, SetParamCustData method [Automation], SetParamCustData method [Automation],ICreateTypeInfo2 interface, _oa96_ICreateTypeInfo2_SetParamCustData, automat.icreatetypeinfo2_setparamcustdata, oaidl/ICreateTypeInfo2::SetParamCustData
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
 - ICreateTypeInfo2::SetParamCustData
 - oaidl/ICreateTypeInfo2::SetParamCustData
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
 - ICreateTypeInfo2.SetParamCustData
---

# ICreateTypeInfo2::SetParamCustData


## -description

 Sets a value for the custom data for the specified parameter.

## -parameters

### -param indexFunc [in]

The index of the function for which to set the custom data.

### -param indexParam [in]

The index of the parameter of the function for which to set the custom data.

### -param guid [in]

The globally unique identifier (GUID) used to identify the data.

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