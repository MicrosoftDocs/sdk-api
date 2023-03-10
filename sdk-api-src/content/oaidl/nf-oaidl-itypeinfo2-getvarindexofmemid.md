---
UID: NF:oaidl.ITypeInfo2.GetVarIndexOfMemId
title: ITypeInfo2::GetVarIndexOfMemId (oaidl.h)
description: Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member). (ITypeInfo2.GetVarIndexOfMemId)
helpviewer_keywords: ["GetVarIndexOfMemId","GetVarIndexOfMemId method [Automation]","GetVarIndexOfMemId method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetVarIndexOfMemId method","ITypeInfo2.GetVarIndexOfMemId","ITypeInfo2::GetVarIndexOfMemId","_oa96_ITypeInfo2_GetVarIndexOfMemId","automat.itypeinfo2_getvarindexofmemid","oaidl/ITypeInfo2::GetVarIndexOfMemId"]
old-location: automat\itypeinfo2_getvarindexofmemid.htm
tech.root: automat
ms.assetid: 6b97ddbf-bcb3-4e39-a355-40c1fd4e8c6a
ms.date: 12/05/2018
ms.keywords: GetVarIndexOfMemId, GetVarIndexOfMemId method [Automation], GetVarIndexOfMemId method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetVarIndexOfMemId method, ITypeInfo2.GetVarIndexOfMemId, ITypeInfo2::GetVarIndexOfMemId, _oa96_ITypeInfo2_GetVarIndexOfMemId, automat.itypeinfo2_getvarindexofmemid, oaidl/ITypeInfo2::GetVarIndexOfMemId
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
 - ITypeInfo2::GetVarIndexOfMemId
 - oaidl/ITypeInfo2::GetVarIndexOfMemId
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
 - ITypeInfo2.GetVarIndexOfMemId
---

# ITypeInfo2::GetVarIndexOfMemId


## -description

Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

## -parameters

### -param memid [in]

The member identifier.

### -param pVarIndex [out]

The index.

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
