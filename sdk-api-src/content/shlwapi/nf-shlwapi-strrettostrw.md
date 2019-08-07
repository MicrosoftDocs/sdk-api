---
UID: NF:shlwapi.StrRetToStrW
title: StrRetToStrW function (shlwapi.h)
author: windows-sdk-content
description: Takes an STRRET structure returned by IShellFolder::GetDisplayNameOf and returns a pointer to an allocated string containing the display name.
old-location: shell\StrRetToStr.htm
tech.root: shell
ms.assetid: 03b0dffb-8ef7-41da-9773-81ed55275802
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StrRetToStr, StrRetToStr function [Windows Shell], StrRetToStrA, StrRetToStrW, _win32_StrRetToStr, shell.StrRetToStr, shlwapi/StrRetToStr, shlwapi/StrRetToStrA, shlwapi/StrRetToStrW
ms.topic: function
f1_keywords:
- shlwapi/StrRetToStr
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrRetToStrW function


## -description


Takes an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure returned by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> and returns a pointer to an allocated string containing the display name.


## -parameters




### -param pstr [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. When the function returns, this pointer will no longer be valid.


### -param pidl [in, optional]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a> structure. This value can be <b>NULL</b>.


### -param ppsz [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated string containing the result. <b>StrRetToStr</b> allocates memory for this string with <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. You should free the string with <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a>
 

 

