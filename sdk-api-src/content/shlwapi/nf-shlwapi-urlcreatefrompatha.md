---
UID: NF:shlwapi.UrlCreateFromPathA
title: UrlCreateFromPathA function (shlwapi.h)
description: Converts a Microsoft MS-DOS path to a canonicalized URL. (ANSI)
helpviewer_keywords: ["UrlCreateFromPathA", "shlwapi/UrlCreateFromPathA"]
old-location: shell\UrlCreateFromPath.htm
tech.root: shell
ms.assetid: b69ab203-daab-4951-b3b9-c5ca37c532b3
ms.date: 12/05/2018
ms.keywords: UrlCreateFromPath, UrlCreateFromPath function [Windows Shell], UrlCreateFromPathA, UrlCreateFromPathW, _win32_UrlCreateFromPath, shell.UrlCreateFromPath, shlwapi/UrlCreateFromPath, shlwapi/UrlCreateFromPathA, shlwapi/UrlCreateFromPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlCreateFromPathW (Unicode) and UrlCreateFromPathA (ANSI)
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
 - UrlCreateFromPathA
 - shlwapi/UrlCreateFromPathA
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
 - UrlCreateFromPath
 - UrlCreateFromPathA
 - UrlCreateFromPathW
---

# UrlCreateFromPathA function


## -description

Converts a Microsoft MS-DOS path to a canonicalized URL.

## -parameters

### -param pszPath [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the MS-DOS path.

### -param pszUrl [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the URL.

### -param pcchUrl [in, out]

Type: <b>DWORD*</b>

The number of characters in <i>pszUrl</i>.

### -param dwFlags

Type: <b>DWORD</b>

Reserved. Set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_FALSE if <i>pszPath</i> is already in URL format. In this case, <i>pszPath</i> will simply be copied to <i>pszUrl</i>. Otherwise, it returns S_OK if successful or a standard COM error value if not.

## -remarks

<div class="alert"><b>Note</b>  <b>UrlCreateFromPath</b> does not support extended paths. These are paths that include the extended-length path prefix "\\?\".</div>
<div> </div>



> [!NOTE]
> The shlwapi.h header defines UrlCreateFromPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

