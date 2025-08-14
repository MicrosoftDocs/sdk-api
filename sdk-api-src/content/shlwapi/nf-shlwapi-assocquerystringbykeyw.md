---
UID: NF:shlwapi.AssocQueryStringByKeyW
title: AssocQueryStringByKeyW function (shlwapi.h)
description: Searches for and retrieves a file association-related string from the registry starting from a specified key. (Unicode)
helpviewer_keywords: ["AssocQueryStringByKey", "AssocQueryStringByKey function [Windows Shell]", "AssocQueryStringByKeyW", "_win32_AssocQueryStringByKey", "shell.AssocQueryStringByKey", "shlwapi/AssocQueryStringByKey", "shlwapi/AssocQueryStringByKeyW"]
old-location: shell\AssocQueryStringByKey.htm
tech.root: shell
ms.assetid: 6816f7fe-9a70-4c5f-bd45-d1ca96d4ebd0
ms.date: 12/05/2018
ms.keywords: AssocQueryStringByKey, AssocQueryStringByKey function [Windows Shell], AssocQueryStringByKeyA, AssocQueryStringByKeyW, _win32_AssocQueryStringByKey, shell.AssocQueryStringByKey, shlwapi/AssocQueryStringByKey, shlwapi/AssocQueryStringByKeyA, shlwapi/AssocQueryStringByKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AssocQueryStringByKeyW (Unicode) and AssocQueryStringByKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AssocQueryStringByKeyW
 - shlwapi/AssocQueryStringByKeyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - AssocQueryStringByKey
 - AssocQueryStringByKeyA
 - AssocQueryStringByKeyW
---

# AssocQueryStringByKeyW function


## -description

Searches for and retrieves a file association-related string from the registry starting from a specified key.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

The flags that can be used to control the search. It can be any combination of <a href="/windows/win32/shell/assocf_str">ASSOCF</a> values, except that only one ASSOCF_INIT value can be included.

### -param str [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a> value that specifies the type of string that is to be returned.

### -param hkAssoc [in]

Type: <b>HKEY</b>

The HKEY value of the key that will be used as a root key. The search looks only below this key.

### -param pszExtra [in, optional]

Type: <b>LPCTSTR</b>

A pointer to an optional null-terminated string with additional information about the location of the string. It is normally set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.

### -param pszOut [out, optional]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string used to return the requested string. Set this parameter to <b>NULL</b> to retrieve the required buffer size.

### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, specifies the number of characters in the <i>pszOut</i> buffer. When the function returns, it points to the number of characters placed in the buffer. 

                    

If the <a href="/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF_NOTRUNCATE</a> flag is set in <i>flags</i> and the buffer specified in <i>pszOut</i> is too small, the function returns E_POINTER and the value is set to the required size of the buffer.

If <i>pszOut</i> is <b>NULL</b>, the function returns S_FALSE and <i>pcchOut</i> points to the required size of the buffer.

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
<td>The <i>pszOut</i> buffer is too small to hold the entire string.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td><i>pszOut</i> is <b>NULL</b>. <i>pcchOut</i> contains the required buffer size.</td>
</tr>
</table>

## -remarks

This function is a wrapper for the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface. It is intended to simplify the process of using this interface. For further discussion of how the file association functions work, see <b>IQueryAssociations</b>.




> [!NOTE]
> The shlwapi.h header defines AssocQueryStringByKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
