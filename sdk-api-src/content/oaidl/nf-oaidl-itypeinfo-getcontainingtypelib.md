---
UID: NF:oaidl.ITypeInfo.GetContainingTypeLib
title: ITypeInfo::GetContainingTypeLib (oaidl.h)
description: Retrieves the containing type library and the index of the type description within that type library.
helpviewer_keywords: ["GetContainingTypeLib","GetContainingTypeLib method [Automation]","GetContainingTypeLib method [Automation]","ITypeInfo interface","ITypeInfo interface [Automation]","GetContainingTypeLib method","ITypeInfo.GetContainingTypeLib","ITypeInfo::GetContainingTypeLib","_oa96_ITypeInfo_GetContainingTypeLib","automat.itypeinfo_getcontainingtypelib","oaidl/ITypeInfo::GetContainingTypeLib"]
old-location: automat\itypeinfo_getcontainingtypelib.htm
tech.root: automat
ms.assetid: 9ca58285-4778-4c2a-b800-dcda9b62e328
ms.date: 12/05/2018
ms.keywords: GetContainingTypeLib, GetContainingTypeLib method [Automation], GetContainingTypeLib method [Automation],ITypeInfo interface, ITypeInfo interface [Automation],GetContainingTypeLib method, ITypeInfo.GetContainingTypeLib, ITypeInfo::GetContainingTypeLib, _oa96_ITypeInfo_GetContainingTypeLib, automat.itypeinfo_getcontainingtypelib, oaidl/ITypeInfo::GetContainingTypeLib
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
 - ITypeInfo::GetContainingTypeLib
 - oaidl/ITypeInfo::GetContainingTypeLib
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
 - ITypeInfo.GetContainingTypeLib
---

# ITypeInfo::GetContainingTypeLib


## -description

Retrieves the containing type library and the index of the type description within that type library.

## -parameters

### -param ppTLib [out]

The containing type library.

### -param pIndex [out]

The index of the type description within the containing type library.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
OLE could not find an implementation of one or more required interfaces.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>