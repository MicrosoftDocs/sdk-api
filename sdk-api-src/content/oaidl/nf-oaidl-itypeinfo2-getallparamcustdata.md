---
UID: NF:oaidl.ITypeInfo2.GetAllParamCustData
title: ITypeInfo2::GetAllParamCustData (oaidl.h)
description: Gets all of the custom data for the specified function parameter.
helpviewer_keywords: ["GetAllParamCustData","GetAllParamCustData method [Automation]","GetAllParamCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetAllParamCustData method","ITypeInfo2.GetAllParamCustData","ITypeInfo2::GetAllParamCustData","_oa96_ITypeInfo2_GetAllParamCustData","automat.itypeinfo2_getallparamcustdata","oaidl/ITypeInfo2::GetAllParamCustData"]
old-location: automat\itypeinfo2_getallparamcustdata.htm
tech.root: automat
ms.assetid: cb5ab67e-b5ff-40fd-a25f-d8dfb1e2c636
ms.date: 12/05/2018
ms.keywords: GetAllParamCustData, GetAllParamCustData method [Automation], GetAllParamCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetAllParamCustData method, ITypeInfo2.GetAllParamCustData, ITypeInfo2::GetAllParamCustData, _oa96_ITypeInfo2_GetAllParamCustData, automat.itypeinfo2_getallparamcustdata, oaidl/ITypeInfo2::GetAllParamCustData
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
 - ITypeInfo2::GetAllParamCustData
 - oaidl/ITypeInfo2::GetAllParamCustData
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
 - ITypeInfo2.GetAllParamCustData
---

# ITypeInfo2::GetAllParamCustData


## -description

Gets all of the custom data for the specified function parameter.

## -parameters

### -param indexFunc [in]

The index of the function for which to get the custom data.

### -param indexParam [in]

The index of the parameter of this function for which to get the custom data.

### -param pCustData [out]

The custom data items.

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