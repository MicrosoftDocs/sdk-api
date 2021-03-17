---
UID: NF:oaidl.ITypeLib.GetTypeInfoOfGuid
title: ITypeLib::GetTypeInfoOfGuid (oaidl.h)
description: Retrieves the type description that corresponds to the specified GUID.
helpviewer_keywords: ["GetTypeInfoOfGuid","GetTypeInfoOfGuid method [Automation]","GetTypeInfoOfGuid method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","GetTypeInfoOfGuid method","ITypeLib.GetTypeInfoOfGuid","ITypeLib::GetTypeInfoOfGuid","_oa96_ITypeLib_GetTypeInfoOfGuid","automat.itypelib_gettypeinfoofguid","oaidl/ITypeLib::GetTypeInfoOfGuid"]
old-location: automat\itypelib_gettypeinfoofguid.htm
tech.root: automat
ms.assetid: 58f96322-f1cd-448c-906d-b7faa65ab9a0
ms.date: 12/05/2018
ms.keywords: GetTypeInfoOfGuid, GetTypeInfoOfGuid method [Automation], GetTypeInfoOfGuid method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeInfoOfGuid method, ITypeLib.GetTypeInfoOfGuid, ITypeLib::GetTypeInfoOfGuid, _oa96_ITypeLib_GetTypeInfoOfGuid, automat.itypelib_gettypeinfoofguid, oaidl/ITypeLib::GetTypeInfoOfGuid
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
 - ITypeLib::GetTypeInfoOfGuid
 - oaidl/ITypeLib::GetTypeInfoOfGuid
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
 - ITypeLib.GetTypeInfoOfGuid
---

# ITypeLib::GetTypeInfoOfGuid


## -description

Retrieves the type description that corresponds to the specified GUID.

## -parameters

### -param guid [in]

The GUID of the type description.

### -param ppTinfo [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> interface.

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
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No type description was found in the library with the specified GUID.

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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>