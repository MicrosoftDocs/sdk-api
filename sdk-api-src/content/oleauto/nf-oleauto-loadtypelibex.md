---
UID: NF:oleauto.LoadTypeLibEx
title: LoadTypeLibEx function (oleauto.h)
description: Loads a type library and (optionally) registers it in the system registry.  .
helpviewer_keywords: ["LoadTypeLibEx","LoadTypeLibEx function [Automation]","_oa96_LoadTypeLibEx","automat.loadtypelibex","oleauto/LoadTypeLibEx"]
old-location: automat\loadtypelibex.htm
tech.root: automat
ms.assetid: 56a7f9e1-810b-4a42-aa4d-691f4304f5ef
ms.date: 12/05/2018
ms.keywords: LoadTypeLibEx, LoadTypeLibEx function [Automation], _oa96_LoadTypeLibEx, automat.loadtypelibex, oleauto/LoadTypeLibEx
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
 - LoadTypeLibEx
 - oleauto/LoadTypeLibEx
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
 - LoadTypeLibEx
---

# LoadTypeLibEx function


## -description

Loads a type library and (optionally) registers it in the system registry.

## -parameters

### -param szFile

The type library file.

### -param regkind

Identifies the kind of registration to perform for the type library based on the following flags: DEFAULT, REGISTER and NONE. REGKIND_DEFAULT simply calls LoadTypeLib and registration occurs based on the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelib">LoadTypeLib</a> registration rules. REGKIND_NONE calls <b>LoadTypeLib</b> without the registration process enabled. REGKIND_REGISTER calls <b>LoadTypeLib</b> followed by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a>, which registers the type library. To unregister the type library, use <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-unregistertypelib">UnRegisterTypeLib</a>.

### -param pptlib

The type library.

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
<dt><b>TYPE_E_REGISTRYACCESS
</b></dt>
</dl>
</td>
<td width="60%">
The system registration database could not be opened.


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
<dt><b>TYPE_E_CANTLOADLIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The type library or DLL could not be loaded.

</td>
</tr>
</table>

## -remarks

Enables programmers to specify whether or not the type library should be loaded.