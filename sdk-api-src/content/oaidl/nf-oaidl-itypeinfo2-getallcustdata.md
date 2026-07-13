---
UID: NF:oaidl.ITypeInfo2.GetAllCustData
title: ITypeInfo2::GetAllCustData (oaidl.h)
description: Gets all custom data items for the library. (ITypeInfo2.GetAllCustData)
helpviewer_keywords: ["GetAllCustData","GetAllCustData method [Automation]","GetAllCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetAllCustData method","ITypeInfo2.GetAllCustData","ITypeInfo2::GetAllCustData","_oa96_ITypeInfo2_GetAllCustData","automat.itypeinfo2_getallcustdata","oaidl/ITypeInfo2::GetAllCustData"]
old-location: automat\itypeinfo2_getallcustdata.htm
tech.root: automat
ms.assetid: ba91134e-0d0a-4f33-a527-700f83344055
ms.date: 12/05/2018
ms.keywords: GetAllCustData, GetAllCustData method [Automation], GetAllCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetAllCustData method, ITypeInfo2.GetAllCustData, ITypeInfo2::GetAllCustData, _oa96_ITypeInfo2_GetAllCustData, automat.itypeinfo2_getallcustdata, oaidl/ITypeInfo2::GetAllCustData
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
 - ITypeInfo2::GetAllCustData
 - oaidl/ITypeInfo2::GetAllCustData
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
 - ITypeInfo2.GetAllCustData
---

# ITypeInfo2::GetAllCustData


## -description

Gets all custom data items for the library.

## -parameters

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

## -remarks

After the call, the caller needs to release memory used to hold the custom data item by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-clearcustdata">ClearCustData</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>
