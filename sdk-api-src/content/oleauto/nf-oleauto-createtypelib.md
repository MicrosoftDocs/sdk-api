---
UID: NF:oleauto.CreateTypeLib
title: CreateTypeLib function (oleauto.h)
description: Provides access to a new object instance that supports the ICreateTypeLib interface.
helpviewer_keywords: ["CreateTypeLib","CreateTypeLib function [Automation]","_oa96_CreateTypeLib","automat.createtypelib","oleauto/CreateTypeLib"]
old-location: automat\createtypelib.htm
tech.root: automat
ms.assetid: c7a94d5b-7ac5-4b7c-8aed-ead23de9ea75
ms.date: 12/05/2018
ms.keywords: CreateTypeLib, CreateTypeLib function [Automation], _oa96_CreateTypeLib, automat.createtypelib, oleauto/CreateTypeLib
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateTypeLib
 - oleauto/CreateTypeLib
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - CreateTypeLib
---

# CreateTypeLib function


## -description

Provides access to a new object instance that supports the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> interface.

## -parameters

### -param syskind

The target operating system for which to create a type library.

### -param szFile

The name of the file to create.

### -param ppctlib

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> interface.

## -returns

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
<dt><b>STG_E_INSUFFICIENTMEMORY
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
<dt><b>TYPE_E_IOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function could not create the file.


</td>
</tr>
</table>
 

This method can also return the FACILITY_STORAGE errors.

## -remarks

<b>CreateTypeLib</b> sets its output parameter (ppctlib) to point to a newly created object that supports the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypelib">ICreateTypeLib</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/automat/type-building-functions">Type Building Functions</a>