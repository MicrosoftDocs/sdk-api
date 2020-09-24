---
UID: NF:oaidl.ITypeLib2.GetLibStatistics
title: ITypeLib2::GetLibStatistics (oaidl.h)
description: Returns statistics about a type library that are required for efficient sizing of hash tables.
helpviewer_keywords: ["GetLibStatistics","GetLibStatistics method [Automation]","GetLibStatistics method [Automation]","ITypeLib2 interface","ITypeLib2 interface [Automation]","GetLibStatistics method","ITypeLib2.GetLibStatistics","ITypeLib2::GetLibStatistics","_oa96_ITypeLib2_GetLibStatistics","automat.itypelib2_getlibstatistics","oaidl/ITypeLib2::GetLibStatistics"]
old-location: automat\itypelib2_getlibstatistics.htm
tech.root: automat
ms.assetid: b6ee47f7-eca6-48f6-b984-ff8c83a4ca46
ms.date: 12/05/2018
ms.keywords: GetLibStatistics, GetLibStatistics method [Automation], GetLibStatistics method [Automation],ITypeLib2 interface, ITypeLib2 interface [Automation],GetLibStatistics method, ITypeLib2.GetLibStatistics, ITypeLib2::GetLibStatistics, _oa96_ITypeLib2_GetLibStatistics, automat.itypelib2_getlibstatistics, oaidl/ITypeLib2::GetLibStatistics
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
 - ITypeLib2::GetLibStatistics
 - oaidl/ITypeLib2::GetLibStatistics
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
 - ITypeLib2.GetLibStatistics
---

# ITypeLib2::GetLibStatistics


## -description

Returns statistics about a type library that are required for efficient sizing of hash tables.

## -parameters

### -param pcUniqueNames [out]

A count of unique names. If the caller does not need this information, set to NULL.

### -param pcchUniqueNames [out]

A change in the count of unique names.

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