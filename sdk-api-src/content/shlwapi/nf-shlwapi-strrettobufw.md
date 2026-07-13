---
UID: NF:shlwapi.StrRetToBufW
title: StrRetToBufW function (shlwapi.h)
description: Converts an STRRET structure returned by IShellFolder::GetDisplayNameOf to a string, and places the result in a buffer. (Unicode)
helpviewer_keywords: ["StrRetToBuf", "StrRetToBuf function [Windows Shell]", "StrRetToBufW", "_win32_StrRetToBuf", "shell.StrRetToBuf", "shlwapi/StrRetToBuf", "shlwapi/StrRetToBufW"]
old-location: shell\StrRetToBuf.htm
tech.root: shell
ms.assetid: 89dab3ee-e9f8-499a-97ec-6fe732315891
ms.date: 12/05/2018
ms.keywords: StrRetToBuf, StrRetToBuf function [Windows Shell], StrRetToBufA, StrRetToBufW, _win32_StrRetToBuf, shell.StrRetToBuf, shlwapi/StrRetToBuf, shlwapi/StrRetToBufA, shlwapi/StrRetToBufW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrRetToBufW (Unicode) and StrRetToBufA (ANSI)
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
 - StrRetToBufW
 - shlwapi/StrRetToBufW
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
 - ext-ms-win-shell-shlwapi-l1-1-2.dll
 - Shlwapi.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrRetToBuf
 - StrRetToBufA
 - StrRetToBufW
---

# StrRetToBufW function


## -description

Converts an <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> to a string, and places the result in a buffer.

## -parameters

### -param pstr [in, out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. When the function returns, this pointer will no longer be valid.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

### -param pszBuf [out]

Type: <b>LPTSTR</b>

A buffer to hold the display name. It will be returned as a null-terminated string. If <i>cchBuf</i> is too small, the name will be truncated to fit.

### -param cchBuf [in]

Type: <b>UINT</b>

The size of <i>pszBuf</i>, in characters. If <i>cchBuf</i> is too small, the string will be truncated to fit.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <b>uType</b> member of the structure pointed to by <i>pstr</i> is set to <b>STRRET_WSTR</b>, the <b>pOleStr</b> member of that structure will be freed on return.





> [!NOTE]
> The shlwapi.h header defines StrRetToBuf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>



<a href="/windows/desktop/shell/consts-enums-flags">StrRetToStrN</a>
