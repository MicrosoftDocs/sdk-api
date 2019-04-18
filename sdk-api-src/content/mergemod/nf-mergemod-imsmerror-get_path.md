---
UID: NF:mergemod.IMsmError.get_Path
title: IMsmError::get_Path (mergemod.h)
author: windows-sdk-content
description: The get_Path method retrieves the Path property of the Error object.
old-location: setup\imsmerror_get_path.htm
tech.root: Msi
ms.assetid: a431f0c6-6551-4983-8638-0a76cada822d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMsmError interface,get_Path method, IMsmError.get_Path, IMsmError::get_Path, _msi_get_path_function, get_Path, get_Path method, get_Path method,IMsmError interface, mergemod/IMsmError::get_Path, setup.imsmerror_get_path
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError.get_Path
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmError::get_Path


## -description


The 
<b>get_Path</b> method retrieves the 
<a href="https://msdn.microsoft.com/b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b">Path</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.


## -parameters




### -param ErrorPath [out]

A pointer to a location in memory that is filled in with a <b>BSTR</b> value.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Path is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system was unable to allocate memory for the string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



The client is responsible for freeing the resulting string using <b>SysFreeString</b>.

In Windows Installer versions 1.0 and 1.1 
<b>get_Path</b> always returns the empty string. Future versions of the class may use this function to return the path to the file or directory that could not be created. This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate. You can determine the type of error by calling <a href="https://msdn.microsoft.com/733a5390-419d-414a-b50e-8400d179bfb6">IMsmError::get_Type</a>.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

