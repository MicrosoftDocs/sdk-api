---
UID: NF:shlwapi.IQueryAssociations.GetString
title: IQueryAssociations::GetString
author: windows-sdk-content
description: Searches for and retrieves a file or protocol association-related string from the registry.
old-location: shell\IQueryAssociations_GetString.htm
tech.root: shell
ms.assetid: 72463664-783b-4375-a6ba-43633a82ec7e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetString, GetString method [Windows Shell], GetString method [Windows Shell],IQueryAssociations interface, IQueryAssociations interface [Windows Shell],GetString method, IQueryAssociations.GetString, IQueryAssociations::GetString, _win32_IQueryAssociations_GetString, shell.IQueryAssociations_GetString, shlwapi/IQueryAssociations::GetString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryAssociations.GetString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shlwapi.h
: 
- IQueryAssociations.GetString
: 
---

# IQueryAssociations::GetString


## -description


Searches for and retrieves a file or protocol association-related string from the registry.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a></b>

A flag that can be used to control the search. It can be any combination of the following <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a> values. 

					

<ul>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_IGNOREBASECLASS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_NOFIXUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_NOTRUNCATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_NOUSERSETTINGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_REMAPRUNDLL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_VERIFY</a>
</li>
</ul>

### -param str [in]

Type: <b><a href="https://msdn.microsoft.com/b5fd3d25-3630-4dd8-acd2-d2e4ed571604">ASSOCSTR</a></b>

An <a href="https://msdn.microsoft.com/b5fd3d25-3630-4dd8-acd2-d2e4ed571604">ASSOCSTR</a> value that specifies the type of string that is to be returned.


### -param pszExtra [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional, null-terminated Unicode string with information about the location of the string. It is typically set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.


### -param pszOut [out, optional]

Type: <b>LPWSTR</b>

A pointer to a null-terminated Unicode string used to return the requested string. Set this parameter to <b>NULL</b> to retrieve the required buffer size.


### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pwszOut</i> buffer. When the function returns successfully, it points to the number of characters placed in the buffer.

If the <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_NOTRUNCATE</a> flag is set in <i>flags</i> and the buffer specified in <i>pwszOut</i> is too small, the function returns E_POINTER and <i>pcchOut</i> points to the required size of the buffer.

If <i>pwszOut</i> is <b>NULL</b>, the function returns S_FALSE and <i>pcchOut</i> points to the required size of the buffer.


## -returns



Type: <b>HRESULT</b>

Returns a standard COM error value, including the following: 

                    

<table class="clsStd">
<tr>
<th>Error</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
<tr>
<td>E_POINTER</td>
<td>The <i>pwszOut</i> buffer is too small to hold the entire string.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td><i>pwszOut</i> is <b>NULL</b>. <i>pcchOut</i> contains the required buffer size.</td>
</tr>
</table>
 



