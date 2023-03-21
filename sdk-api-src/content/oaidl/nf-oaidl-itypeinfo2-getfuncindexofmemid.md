---
UID: NF:oaidl.ITypeInfo2.GetFuncIndexOfMemId
title: ITypeInfo2::GetFuncIndexOfMemId (oaidl.h)
description: Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member). (ITypeInfo2.GetFuncIndexOfMemId)
helpviewer_keywords: ["GetFuncIndexOfMemId","GetFuncIndexOfMemId method [Automation]","GetFuncIndexOfMemId method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetFuncIndexOfMemId method","ITypeInfo2.GetFuncIndexOfMemId","ITypeInfo2::GetFuncIndexOfMemId","_oa96_ITypeInfo2_GetFuncIndexOfMemId","automat.itypeinfo2_getfuncindexofmemid","oaidl/ITypeInfo2::GetFuncIndexOfMemId"]
old-location: automat\itypeinfo2_getfuncindexofmemid.htm
tech.root: automat
ms.assetid: dad5fd34-9322-46aa-9ae3-d5ff9d1639b1
ms.date: 12/05/2018
ms.keywords: GetFuncIndexOfMemId, GetFuncIndexOfMemId method [Automation], GetFuncIndexOfMemId method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetFuncIndexOfMemId method, ITypeInfo2.GetFuncIndexOfMemId, ITypeInfo2::GetFuncIndexOfMemId, _oa96_ITypeInfo2_GetFuncIndexOfMemId, automat.itypeinfo2_getfuncindexofmemid, oaidl/ITypeInfo2::GetFuncIndexOfMemId
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
 - ITypeInfo2::GetFuncIndexOfMemId
 - oaidl/ITypeInfo2::GetFuncIndexOfMemId
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
 - ITypeInfo2.GetFuncIndexOfMemId
---

# ITypeInfo2::GetFuncIndexOfMemId


## -description

Binds to a specific member based on a known DISPID, where the member name is not known (for example, when binding to a default member).

## -parameters

### -param memid [in]

The member identifier.

### -param invKind [in]

The invoke kind.

### -param pFuncIndex [out]

An index into the function.

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
