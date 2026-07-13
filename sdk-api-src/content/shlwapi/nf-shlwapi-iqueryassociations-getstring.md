---
UID: NF:shlwapi.IQueryAssociations.GetString
title: IQueryAssociations::GetString (shlwapi.h)
description: Searches for and retrieves a file or protocol association-related string from the registry. (IQueryAssociations.GetString)
helpviewer_keywords: ["GetString","GetString method [Windows Shell]","GetString method [Windows Shell]","IQueryAssociations interface","IQueryAssociations interface [Windows Shell]","GetString method","IQueryAssociations.GetString","IQueryAssociations::GetString","_win32_IQueryAssociations_GetString","shell.IQueryAssociations_GetString","shlwapi/IQueryAssociations::GetString"]
old-location: shell\IQueryAssociations_GetString.htm
tech.root: shell
ms.assetid: 72463664-783b-4375-a6ba-43633a82ec7e
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Windows Shell], GetString method [Windows Shell],IQueryAssociations interface, IQueryAssociations interface [Windows Shell],GetString method, IQueryAssociations.GetString, IQueryAssociations::GetString, _win32_IQueryAssociations_GetString, shell.IQueryAssociations_GetString, shlwapi/IQueryAssociations::GetString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryAssociations::GetString
 - shlwapi/IQueryAssociations::GetString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryAssociations.GetString
---

# IQueryAssociations::GetString


## -description

Searches for and retrieves a file or protocol association-related string from the registry.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

A flag that can be used to control the search. It can be any combination of the following <a href="/windows/win32/shell/assocf_str">ASSOCF</a> values.

<ul>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_IGNOREBASECLASS</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_NOFIXUPS</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_NOTRUNCATE</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_NOUSERSETTINGS</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_REMAPRUNDLL</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_VERIFY</a>
</li>
</ul>

### -param str [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a></b>

An <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a> value that specifies the type of string that is to be returned.

### -param pszExtra [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional, null-terminated Unicode string with information about the location of the string. It is typically set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.

### -param pszOut [out, optional]

Type: <b>LPWSTR</b>

A pointer to a null-terminated Unicode string used to return the requested string. Set this parameter to <b>NULL</b> to retrieve the required buffer size.

### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pwszOut</i> buffer. When the function returns successfully, it points to the number of characters placed in the buffer.

If the <a href="/windows/win32/shell/assocf_str">ASSOCF_NOTRUNCATE</a> flag is set in <i>flags</i> and the buffer specified in <i>pwszOut</i> is too small, the function returns E_POINTER and <i>pcchOut</i> points to the required size of the buffer.

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
