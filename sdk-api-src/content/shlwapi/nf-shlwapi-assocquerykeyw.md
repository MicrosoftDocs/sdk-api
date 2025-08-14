---
UID: NF:shlwapi.AssocQueryKeyW
title: AssocQueryKeyW function (shlwapi.h)
description: Searches for and retrieves a key related to a file or protocol association from the registry. (Unicode)
helpviewer_keywords: ["AssocQueryKey", "AssocQueryKey function [Windows Shell]", "AssocQueryKeyW", "CLSID", "Executable name", "File name extension", "ProgID", "_win32_AssocQueryKey", "shell.AssocQueryKey", "shlwapi/AssocQueryKey", "shlwapi/AssocQueryKeyW"]
old-location: shell\AssocQueryKey.htm
tech.root: shell
ms.assetid: 9eaeb885-0428-48c3-82a7-5dc21d5015ce
ms.date: 12/05/2018
ms.keywords: AssocQueryKey, AssocQueryKey function [Windows Shell], AssocQueryKeyA, AssocQueryKeyW, CLSID, Executable name, File name extension, ProgID, _win32_AssocQueryKey, shell.AssocQueryKey, shlwapi/AssocQueryKey, shlwapi/AssocQueryKeyA, shlwapi/AssocQueryKeyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AssocQueryKeyW (Unicode) and AssocQueryKeyA (ANSI)
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
 - AssocQueryKeyW
 - shlwapi/AssocQueryKeyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - AssocQueryKey
 - AssocQueryKeyA
 - AssocQueryKeyW
---

# AssocQueryKeyW function


## -description

Searches for and retrieves a key related to a file or protocol association from the registry.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

The flags that can be used to control the search. It can be any combination of <a href="/windows/win32/shell/assocf_str">ASSOCF</a> values, except that only one ASSOCF_INIT value can be included.

### -param key [in]

Type: <b><a href="/windows/desktop/api/shlwapi/ne-shlwapi-assockey">ASSOCKEY</a></b>

The <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assockey">ASSOCKEY</a> value that specifies the type of key that is to be returned.

### -param pszAssoc [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that is used to determine the root key. Four types of strings can be used.



#### File name extension

A file name extension, such as .txt.



#### CLSID

A CLSID GUID in the standard "{GUID}" format.



#### ProgID

An application's ProgID, such as <b>Word.Document.8</b>.



#### Executable name

The name of an application's .exe file. The <a href="/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.

### -param pszExtra [in]

Type: <b>LPCTSTR</b>

A pointer to an optional null-terminated string with additional information about the location of the string. It is normally set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.

### -param phkeyOut [out]

Type: <b>HKEY*</b>

A pointer to the key's HKEY value.


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

Returns S_OK if successful, or a COM error value otherwise.

## -remarks

This function is a wrapper for the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface. It is intended to simplify the process of using the interface. For further discussion of how the file and protocol association functions work, see <b>IQueryAssociations</b>.




> [!NOTE]
> The shlwapi.h header defines AssocQueryKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
