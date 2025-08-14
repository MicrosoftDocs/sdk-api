---
UID: NF:shlwapi.AssocQueryStringW
title: AssocQueryStringW function (shlwapi.h)
description: Searches for and retrieves a file or protocol association-related string from the registry. (AssocQueryStringW)
helpviewer_keywords: ["AssocQueryString", "AssocQueryString function [Windows Shell]", "AssocQueryStringW", "CLSID", "Executable name", "File name extension", "ProgID", "_win32_AssocQueryString", "shell.AssocQueryString", "shlwapi/AssocQueryString", "shlwapi/AssocQueryStringW"]
old-location: shell\AssocQueryString.htm
tech.root: shell
ms.assetid: 026b841d-b831-475e-a788-2c79801e20b8
ms.date: 12/05/2018
ms.keywords: AssocQueryString, AssocQueryString function [Windows Shell], AssocQueryStringA, AssocQueryStringW, CLSID, Executable name, File name extension, ProgID, _win32_AssocQueryString, shell.AssocQueryString, shlwapi/AssocQueryString, shlwapi/AssocQueryStringA, shlwapi/AssocQueryStringW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AssocQueryStringW (Unicode) and AssocQueryStringA (ANSI)
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
 - AssocQueryStringW
 - shlwapi/AssocQueryStringW
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
 - Ext-MS-Win-shell-shlwapi-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - AssocQueryString
 - AssocQueryStringA
 - AssocQueryStringW
---

# AssocQueryStringW function


## -description

Searches for and retrieves a file or protocol association-related string from the registry.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

The flags that can be used to control the search. It can be any combination of <a href="/windows/win32/shell/assocf_str">ASSOCF</a> values, except that only one ASSOCF_INIT value can be included.

### -param str [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR</a> value that specifies the type of string that is to be returned.

### -param pszAssoc [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that is used to determine the root key. The following four types of strings can be used.



#### File name extension

A file name extension, such as .txt.



#### CLSID

A CLSID GUID in the standard "{GUID}" format.



#### ProgID

An application's ProgID, such as <b>Word.Document.8</b>.



#### Executable name

The name of an application's .exe file. The <a href="/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.

### -param pszExtra [in, optional]

Type: <b>LPCTSTR</b>

An optional null-terminated string with additional information about the location of the string. It is typically set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.

### -param pszOut [out, optional]

Type: <b>LPTSTR</b>

Pointer to a null-terminated string that, when this function returns successfully, receives the requested string. Set this parameter to <b>NULL</b> to retrieve the required buffer size.

### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, when calling the function, is set to the number of characters in the <i>pszOut</i> buffer. When the function returns successfully, the value is set to the number of characters actually placed in the buffer.

If the <a href="/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF_NOTRUNCATE</a> flag is set in <i>flags</i> and the buffer specified in <i>pszOut</i> is too small, the function returns E_POINTER and the value is set to the required size of the buffer.

If <i>pszOut</i> is <b>NULL</b>, the function returns S_FALSE and <i>pcchOut</i> points to the required size, in characters, of the buffer.


##### - pszAssoc.CLSID

A CLSID GUID in the standard "{GUID}" format.


##### - pszAssoc.Executable name

The name of an application's .exe file. The <a href="/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.


##### - pszAssoc.File name extension

A file name extension, such as .txt.


##### - pszAssoc.ProgID

An application's ProgID, such as <b>Word.Document.8</b>.

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

This function is a wrapper for the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface. The <b>AssocQueryString</b> function is intended to simplify the process of using <b>IQueryAssociations</b> interface.

Once an item is selected, the host must decide which (if any) preview handler is available for that item. Preview handlers are typically registered on file name extensions or ProgID, but some preview handlers are only instantiated for items within particular shell folders (the MAPI preview handler is associated with any items that came from the MAPI Shell folder, for example). Thus, the host must use <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> to determine which preview handler to use. For further discussion of how the file and protocol association functions work, see <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>.




> [!NOTE]
> The shlwapi.h header defines AssocQueryString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
