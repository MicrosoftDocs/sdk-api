---
UID: NF:oleauto.LoadRegTypeLib
title: LoadRegTypeLib function (oleauto.h)
description: Uses registry information to load a type library.
helpviewer_keywords: ["LoadRegTypeLib","LoadRegTypeLib function [Automation]","_oa96_LoadRegTypeLib","automat.loadregtypelib","oleauto/LoadRegTypeLib"]
old-location: automat\loadregtypelib.htm
tech.root: automat
ms.assetid: 444b7768-2a4e-4de3-9f28-ef63ac23e8bc
ms.date: 12/05/2018
ms.keywords: LoadRegTypeLib, LoadRegTypeLib function [Automation], _oa96_LoadRegTypeLib, automat.loadregtypelib, oleauto/LoadRegTypeLib
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
 - LoadRegTypeLib
 - oleauto/LoadRegTypeLib
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
 - LoadRegTypeLib
---

# LoadRegTypeLib function


## -description

Uses registry information to load a type library.

## -parameters

### -param rguid

The GUID of the library.

### -param wVerMajor

The major version of the library.

### -param wVerMinor

The minor version of the library.

### -param lcid

The national language code of the library.

### -param pptlib

The loaded type library.

## -returns

This function can return one of these values.

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
<dt><b>TYPE_E_IOERROR
</b></dt>
</dl>
</td>
<td width="60%">
The function could not write to the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE
</b></dt>
</dl>
</td>
<td width="60%">
The type library could not be opened.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVDATAREAD
</b></dt>
</dl>
</td>
<td width="60%">
The function could not read from the file.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_UNSUPFORMAT
</b></dt>
</dl>
</td>
<td width="60%">
The type library has an older format.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_UNKNOWNLCID
</b></dt>
</dl>
</td>
<td width="60%">
The LCID could not be found in the OLE-supported DLLs.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_CANTLOADLIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The type library or DLL could not be loaded.

</td>
</tr>
</table>

## -remarks

The function <b>LoadRegTypeLib</b> defers to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelib">LoadTypeLib</a> to load the file.



<b>LoadRegTypeLib</b> compares the requested version numbers against those found in the system registry, and takes one of the following actions: 



<ul>
<li>
If one of the registered libraries exactly matches both the requested major and minor version numbers, then that type library is loaded.



</li>
<li>
If one or more registered type libraries exactly match the requested major version number, and has a greater minor version number than that requested, the one with the greatest minor version number is loaded.



</li>
<li>
If none of the registered type libraries exactly match the requested major version number (or if none of those that do exactly match the major version number also have a minor version number greater than or equal to the requested minor version number), then <b>LoadRegTypeLib</b> returns an error.


</li>
</ul>