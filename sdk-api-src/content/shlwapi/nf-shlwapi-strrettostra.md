---
UID: NF:shlwapi.StrRetToStrA
title: StrRetToStrA function (shlwapi.h)
description: Takes an STRRET structure returned by IShellFolder::GetDisplayNameOf and returns a pointer to an allocated string containing the display name. (ANSI)
helpviewer_keywords: ["StrRetToStrA", "shlwapi/StrRetToStrA"]
old-location: shell\StrRetToStr.htm
tech.root: shell
ms.assetid: 03b0dffb-8ef7-41da-9773-81ed55275802
ms.date: 12/05/2018
ms.keywords: StrRetToStr, StrRetToStr function [Windows Shell], StrRetToStrA, StrRetToStrW, _win32_StrRetToStr, shell.StrRetToStr, shlwapi/StrRetToStr, shlwapi/StrRetToStrA, shlwapi/StrRetToStrW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrRetToStrW (Unicode) and StrRetToStrA (ANSI)
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
 - StrRetToStrA
 - shlwapi/StrRetToStrA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrRetToStr
 - StrRetToStrA
 - StrRetToStrW
---

# StrRetToStrA function


## -description

Takes an <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> and returns a pointer to an allocated string containing the display name.

## -parameters

### -param pstr [in, out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. When the function returns, this pointer will no longer be valid.

### -param pidl [in, optional]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure. This value can be <b>NULL</b>.

### -param ppsz [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated string containing the result. <b>StrRetToStr</b> allocates memory for this string with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. You should free the string with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines StrRetToStr as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
