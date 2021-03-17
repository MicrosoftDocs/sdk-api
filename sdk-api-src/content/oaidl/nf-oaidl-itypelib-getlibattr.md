---
UID: NF:oaidl.ITypeLib.GetLibAttr
title: ITypeLib::GetLibAttr (oaidl.h)
description: Retrieves the structure that contains the library's attributes.
helpviewer_keywords: ["GetLibAttr","GetLibAttr method [Automation]","GetLibAttr method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","GetLibAttr method","ITypeLib.GetLibAttr","ITypeLib::GetLibAttr","_oa96_ITypeLib_GetLibAttr","automat.itypelib_getlibattr","oaidl/ITypeLib::GetLibAttr"]
old-location: automat\itypelib_getlibattr.htm
tech.root: automat
ms.assetid: edc35364-99dc-438b-81de-4f129c0cf50f
ms.date: 12/05/2018
ms.keywords: GetLibAttr, GetLibAttr method [Automation], GetLibAttr method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetLibAttr method, ITypeLib.GetLibAttr, ITypeLib::GetLibAttr, _oa96_ITypeLib_GetLibAttr, automat.itypelib_getlibattr, oaidl/ITypeLib::GetLibAttr
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
 - ITypeLib::GetLibAttr
 - oaidl/ITypeLib::GetLibAttr
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
 - ITypeLib.GetLibAttr
---

# ITypeLib::GetLibAttr


## -description

Retrieves the structure that contains the library's attributes.

## -parameters

### -param ppTLibAttr [out]

 The library's attributes.

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

Use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-releasetlibattr">ITypeLib::ReleaseTLibAttr</a> to free the memory occupied by the TLIBATTR structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>