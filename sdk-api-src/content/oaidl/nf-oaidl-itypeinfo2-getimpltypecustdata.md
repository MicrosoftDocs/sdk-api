---
UID: NF:oaidl.ITypeInfo2.GetImplTypeCustData
title: ITypeInfo2::GetImplTypeCustData (oaidl.h)
description: Gets the custom data of the implementation type.
helpviewer_keywords: ["GetImplTypeCustData","GetImplTypeCustData method [Automation]","GetImplTypeCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetImplTypeCustData method","ITypeInfo2.GetImplTypeCustData","ITypeInfo2::GetImplTypeCustData","_oa96_ITypeInfo2_GetImplTypeCustData","automat.itypeinfo2_getimpltypecustdata","oaidl/ITypeInfo2::GetImplTypeCustData"]
old-location: automat\itypeinfo2_getimpltypecustdata.htm
tech.root: automat
ms.assetid: 1cb30f35-8ef0-482a-bd1f-83445c97fb1f
ms.date: 12/05/2018
ms.keywords: GetImplTypeCustData, GetImplTypeCustData method [Automation], GetImplTypeCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetImplTypeCustData method, ITypeInfo2.GetImplTypeCustData, ITypeInfo2::GetImplTypeCustData, _oa96_ITypeInfo2_GetImplTypeCustData, automat.itypeinfo2_getimpltypecustdata, oaidl/ITypeInfo2::GetImplTypeCustData
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
 - ITypeInfo2::GetImplTypeCustData
 - oaidl/ITypeInfo2::GetImplTypeCustData
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
 - ITypeInfo2.GetImplTypeCustData
---

# ITypeInfo2::GetImplTypeCustData


## -description

Gets the custom data of the implementation type.

## -parameters

### -param index [in]

The index of the implementation type for the custom data.

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