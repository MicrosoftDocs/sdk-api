---
UID: NF:shlwapi.UrlHashA
title: UrlHashA function (shlwapi.h)
description: Hashes a URL string. (ANSI)
helpviewer_keywords: ["UrlHashA", "shlwapi/UrlHashA"]
old-location: shell\UrlHash.htm
tech.root: shell
ms.assetid: 9c0ce709-e097-4501-bee1-b24df9d4828d
ms.date: 12/05/2018
ms.keywords: UrlHash, UrlHash function [Windows Shell], UrlHashA, UrlHashW, _win32_UrlHash, shell.UrlHash, shlwapi/UrlHash, shlwapi/UrlHashA, shlwapi/UrlHashW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlHashW (Unicode) and UrlHashA (ANSI)
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
 - UrlHashA
 - shlwapi/UrlHashA
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
api_name:
 - UrlHash
 - UrlHashA
 - UrlHashW
---

# UrlHashA function


## -description

Hashes a URL string.

## -parameters

### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.

### -param pbHash [out]

Type: <b>BYTE*</b>

A pointer to a buffer that, when this function returns successfully, receives the hashed array.

### -param cbHash

Type: <b>DWORD</b>

The number of elements in the array at <i>pbHash</i>. It should be no larger than 256.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To hash a URL into a single byte, set <i>cbHash</i> = sizeof(BYTE) and <i>pbHash</i> = (LPBYTE)&amp;bHashedValue, where bHashedValue is a one-byte buffer. To hash a URL into a <b>DWORD</b>, set <i>cbHash</i> = sizeof(DWORD) and <i>pbHash</i> = (LPBYTE)&amp;dwHashedValue, where dwHashedValue is a <b>DWORD</b> buffer.





> [!NOTE]
> The shlwapi.h header defines UrlHash as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-hashdata">HashData</a>
