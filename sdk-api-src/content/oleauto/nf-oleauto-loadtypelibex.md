---
UID: NF:oleauto.LoadTypeLibEx
title: LoadTypeLibEx function
author: windows-sdk-content
description: Loads a type library and (optionally) registers it in the system registry.  .
old-location: automat\loadtypelibex.htm
tech.root: automat
ms.assetid: 56a7f9e1-810b-4a42-aa4d-691f4304f5ef
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: LoadTypeLibEx, LoadTypeLibEx function [Automation], _oa96_LoadTypeLibEx, automat.loadtypelibex, oleauto/LoadTypeLibEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LoadTypeLibEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadTypeLibEx function


## -description


Loads a type library and (optionally) registers it in the system registry.   


## -parameters




### -param szFile

The type library file.


### -param regkind

Identifies the kind of registration to perform for the type library based on the following flags: DEFAULT, REGISTER and NONE. REGKIND_DEFAULT simply calls LoadTypeLib and registration occurs based on the <a href="https://msdn.microsoft.com/155b48e5-5438-409e-9342-630a6a500f60">LoadTypeLib</a> registration rules. REGKIND_NONE calls <b>LoadTypeLib</b> without the registration process enabled. REGKIND_REGISTER calls <b>LoadTypeLib</b> followed by <a href="https://msdn.microsoft.com/d0559a57-b1a4-4036-97ed-024d775cb595">RegisterTypeLib</a>, which registers the type library. To unregister the type library, use <a href="https://msdn.microsoft.com/36c763f0-562c-4fc8-9449-b37e993d5f5c">UnRegisterTypeLib</a>.


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




