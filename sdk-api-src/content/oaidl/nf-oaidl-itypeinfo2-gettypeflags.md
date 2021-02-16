---
UID: NF:oaidl.ITypeInfo2.GetTypeFlags
title: ITypeInfo2::GetTypeFlags (oaidl.h)
description: Returns the type flags without any allocations. This returns a flag that expands the type flags without growing the TYPEATTR (type attribute).
helpviewer_keywords: ["GetTypeFlags","GetTypeFlags method [Automation]","GetTypeFlags method [Automation]","ITypeInfo2 interface","ITypeInfo2 interface [Automation]","GetTypeFlags method","ITypeInfo2.GetTypeFlags","ITypeInfo2::GetTypeFlags","_oa96_ITypeInfo2_GetTypeFlags","automat.itypeinfo2_gettypeflags","oaidl/ITypeInfo2::GetTypeFlags"]
old-location: automat\itypeinfo2_gettypeflags.htm
tech.root: automat
ms.assetid: a240caf6-f7a2-41c4-9950-f0d2df1f3e2d
ms.date: 12/05/2018
ms.keywords: GetTypeFlags, GetTypeFlags method [Automation], GetTypeFlags method [Automation],ITypeInfo2 interface, ITypeInfo2 interface [Automation],GetTypeFlags method, ITypeInfo2.GetTypeFlags, ITypeInfo2::GetTypeFlags, _oa96_ITypeInfo2_GetTypeFlags, automat.itypeinfo2_gettypeflags, oaidl/ITypeInfo2::GetTypeFlags
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
 - ITypeInfo2::GetTypeFlags
 - oaidl/ITypeInfo2::GetTypeFlags
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
 - ITypeInfo2.GetTypeFlags
---

# ITypeInfo2::GetTypeFlags


## -description

Returns the type flags without any allocations. This returns a flag that expands the type flags without growing the TYPEATTR (type attribute).

## -parameters

### -param pTypeFlags [out]

A TYPEFLAG value.

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