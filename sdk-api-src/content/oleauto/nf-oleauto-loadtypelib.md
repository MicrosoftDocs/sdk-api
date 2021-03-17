---
UID: NF:oleauto.LoadTypeLib
title: LoadTypeLib function (oleauto.h)
description: Loads and registers a type library.
helpviewer_keywords: ["LoadTypeLib","LoadTypeLib function [Automation]","_oa96_LoadTypeLib","automat.loadtypelib","oleauto/LoadTypeLib"]
old-location: automat\loadtypelib.htm
tech.root: automat
ms.assetid: 155b48e5-5438-409e-9342-630a6a500f60
ms.date: 12/05/2018
ms.keywords: LoadTypeLib, LoadTypeLib function [Automation], _oa96_LoadTypeLib, automat.loadtypelib, oleauto/LoadTypeLib
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
 - LoadTypeLib
 - oleauto/LoadTypeLib
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
 - LoadTypeLib
---

# LoadTypeLib function


## -description

Loads and registers a type library.

## -parameters

### -param szFile

The name of the file from which the method should attempt to load a type library.

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

The function <b>LoadTypeLib</b> loads a type library (usually created with MkTypLib) that is stored in the specified file. If <i>szFile</i> specifies only a file name without any path, <b>LoadTypeLib</b> searches for the file and proceeds as follows:

<ul>
<li>
If the file is a stand-alone type library implemented by Typelib.dll, the library is loaded directly.



</li>
<li>
If the file is a DLL or an executable file, it is loaded. By default, the type library is extracted from the first resource of type <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>. To load a different type of library resource, append an integer index to <i>szFile</i>. For example: 


```cpp
ITypeLib *ptlib;
LoadTypeLib("C:\\MONTANA\\EXE\\MFA.EXE\\3", &ptlib)
```


This statement loads the type library resource 3 from the file Mfa.exe file. 

</li>
<li>
If the file is none of the above, the file name is parsed into a moniker (an object that represents a file-based link source), and then bound to the moniker. This approach allows <b>LoadTypeLib</b> to be used on foreign type libraries, including in-memory type libraries. Foreign type libraries cannot reside in a DLL or an executable file. For more information on monikers, see the COM Programmer's Reference.



</li>
</ul>
If the type library is already loaded, <b>LoadTypeLib</b> increments the type library's reference count and returns a pointer to the type library.



For backward compatibility, <b>LoadTypeLib</b> will register the type library if the path is not specified in the <i>szFile</i> parameter. <b>LoadTypeLib</b> will not register the type library if the path of the type library is specified. It is recommended that <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a> be used to register a type library.