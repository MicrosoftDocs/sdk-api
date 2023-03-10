---
UID: NF:oaidl.ITypeLib2.GetCustData
title: ITypeLib2::GetCustData (oaidl.h)
description: Gets the custom data. (ITypeLib2.GetCustData)
helpviewer_keywords: ["GetCustData","GetCustData method [Automation]","GetCustData method [Automation]","ITypeLib2 interface","ITypeLib2 interface [Automation]","GetCustData method","ITypeLib2.GetCustData","ITypeLib2::GetCustData","_oa96_ITypeLib2_GetCustData","automat.itypelib2_getcustdata","oaidl/ITypeLib2::GetCustData"]
old-location: automat\itypelib2_getcustdata.htm
tech.root: automat
ms.assetid: e2f29070-6768-4734-a3e2-c9258375b33c
ms.date: 12/05/2018
ms.keywords: GetCustData, GetCustData method [Automation], GetCustData method [Automation],ITypeLib2 interface, ITypeLib2 interface [Automation],GetCustData method, ITypeLib2.GetCustData, ITypeLib2::GetCustData, _oa96_ITypeLib2_GetCustData, automat.itypelib2_getcustdata, oaidl/ITypeLib2::GetCustData
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
 - ITypeLib2::GetCustData
 - oaidl/ITypeLib2::GetCustData
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
 - ITypeLib2.GetCustData
---

# ITypeLib2::GetCustData


## -description

Gets the custom data.

## -parameters

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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib2">ITypeLib2</a>
