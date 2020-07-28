---
UID: NF:oaidl.ITypeInfo2.GetCustData
title: ITypeInfo2::GetCustData (oaidl.h)
description: Gets the custom data.
helpviewer_keywords: ["GetCustData","GetCustData method [Automation]","GetCustData method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetCustData method","ITypeInfo2.GetCustData","ITypeInfo2::GetCustData","_oa96_ITypeInfo2_GetCustData","automat.itypeinfo2_getcustdata","oaidl/ITypeInfo2::GetCustData"]
old-location: automat\itypeinfo2_getcustdata.htm
tech.root: automat
ms.assetid: 0c80a357-0967-413f-a211-c3bae8700b36
ms.date: 12/05/2018
ms.keywords: GetCustData, GetCustData method [Automation], GetCustData method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetCustData method, ITypeInfo2.GetCustData, ITypeInfo2::GetCustData, _oa96_ITypeInfo2_GetCustData, automat.itypeinfo2_getcustdata, oaidl/ITypeInfo2::GetCustData
f1_keywords:
- oaidl/ITypeInfo2.GetCustData
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- oaidl.h
api_name:
- ITypeInfo2.GetCustData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITypeInfo2::GetCustData


## -description


Gets the custom data.


## -parameters




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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>
 

 

