---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



The function <b>LoadRegTypeLib</b> defers to <a href="https://msdn.microsoft.com/155b48e5-5438-409e-9342-630a6a500f60">LoadTypeLib</a> to load the file.



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


