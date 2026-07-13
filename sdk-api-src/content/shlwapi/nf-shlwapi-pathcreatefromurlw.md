---
UID: NF:shlwapi.PathCreateFromUrlW
title: PathCreateFromUrlW function (shlwapi.h)
description: Converts a file URL to a Microsoft MS-DOS path. (Unicode)
helpviewer_keywords: ["PathCreateFromUrl", "PathCreateFromUrl function [Windows Shell]", "PathCreateFromUrlW", "_win32_PathCreateFromUrl", "shell.PathCreateFromUrl", "shlwapi/PathCreateFromUrl", "shlwapi/PathCreateFromUrlW"]
old-location: shell\PathCreateFromUrl.htm
tech.root: shell
ms.assetid: f4136c80-a309-4551-be73-f2f24ecd4675
ms.date: 12/05/2018
ms.keywords: PathCreateFromUrl, PathCreateFromUrl function [Windows Shell], PathCreateFromUrlA, PathCreateFromUrlW, _win32_PathCreateFromUrl, shell.PathCreateFromUrl, shlwapi/PathCreateFromUrl, shlwapi/PathCreateFromUrlA, shlwapi/PathCreateFromUrlW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCreateFromUrlW (Unicode) and PathCreateFromUrlA (ANSI)
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
 - PathCreateFromUrlW
 - shlwapi/PathCreateFromUrlW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathCreateFromUrl
 - PathCreateFromUrlA
 - PathCreateFromUrlW
---

# PathCreateFromUrlW function


## -description

Converts a file URL to a Microsoft MS-DOS path.

## -parameters

### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.

### -param pszPath [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the MS-DOS path. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param pcchPath [in, out]

Type: <b>DWORD*</b>

The number of characters in the <i>pszPath</i> buffer.

### -param dwFlags

Type: <b>DWORD</b>

Reserved. Set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathCreateFromUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

