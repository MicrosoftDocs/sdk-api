---
UID: NF:oaidl.ITypeInfo2.GetTypeKind
title: ITypeInfo2::GetTypeKind (oaidl.h)
description: Returns the TYPEKIND enumeration quickly, without doing any allocations.
helpviewer_keywords: ["GetTypeKind","GetTypeKind method [Automation]","GetTypeKind method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetTypeKind method","ITypeInfo2.GetTypeKind","ITypeInfo2::GetTypeKind","_oa96_ITypeInfo2_GetTypeKind","automat.itypeinfo2_gettypekind","oaidl/ITypeInfo2::GetTypeKind"]
old-location: automat\itypeinfo2_gettypekind.htm
tech.root: automat
ms.assetid: 2ad42274-1952-44b4-ac11-93eacc10a9a9
ms.date: 12/05/2018
ms.keywords: GetTypeKind, GetTypeKind method [Automation], GetTypeKind method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetTypeKind method, ITypeInfo2.GetTypeKind, ITypeInfo2::GetTypeKind, _oa96_ITypeInfo2_GetTypeKind, automat.itypeinfo2_gettypekind, oaidl/ITypeInfo2::GetTypeKind
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
 - ITypeInfo2::GetTypeKind
 - oaidl/ITypeInfo2::GetTypeKind
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
 - ITypeInfo2.GetTypeKind
---

# ITypeInfo2::GetTypeKind


## -description

Returns the TYPEKIND enumeration quickly, without doing any allocations.

## -parameters

### -param pTypeKind [out]

A TYPEKIND value.

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