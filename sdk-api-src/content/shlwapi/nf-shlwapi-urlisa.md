---
UID: NF:shlwapi.UrlIsA
title: UrlIsA function (shlwapi.h)
description: Tests whether a URL is a specified type. (ANSI)
helpviewer_keywords: ["UrlIsA", "shlwapi/UrlIsA"]
old-location: shell\UrlIs.htm
tech.root: shell
ms.assetid: 2e83c953-b4c5-4411-90ca-49ffb94ee374
ms.date: 12/05/2018
ms.keywords: URLIS_APPLIABLE, URLIS_DIRECTORY, URLIS_FILEURL, URLIS_HASQUERY, URLIS_NOHISTORY, URLIS_OPAQUE, URLIS_URL, UrlIs, UrlIs function [Windows Shell], UrlIsA, UrlIsW, _win32_UrlIs, shell.UrlIs, shlwapi/UrlIs, shlwapi/UrlIsA, shlwapi/UrlIsW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsW (Unicode) and UrlIsA (ANSI)
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
 - UrlIsA
 - shlwapi/UrlIsA
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
 - UrlIs
 - UrlIsA
 - UrlIsW
---

# UrlIsA function


## -description

Tests whether a URL is a specified type.

## -parameters

### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.

### -param UrlIs

Type: <b>URLIS</b>

The type of URL to be tested for. This parameter can take one of the following values.



#### URLIS_APPLIABLE

Attempt to determine a valid scheme for the URL.



#### URLIS_DIRECTORY

Does the URL string end with a directory?



#### URLIS_FILEURL

Is the URL a file URL?



#### URLIS_HASQUERY

Does the URL have an appended query string?



#### URLIS_NOHISTORY

Is the URL a URL that is not typically tracked in navigation history?



#### URLIS_OPAQUE

Is the URL <a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisopaquea">opaque</a>?



#### URLIS_URL

Is the URL valid?

## -returns

Type: <b>BOOL</b>

For all but one of the URL types, <b>UrlIs</b> returns <b>TRUE</b> if the URL is the specified type, or <b>FALSE</b> if not. 

                    

If <i>UrlIs</i> is set to <b>URLIS_APPLIABLE</b>, <b>UrlIs</b> will attempt to determine the URL scheme. If the function is able to determine a scheme, it returns <b>TRUE</b>, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisfileurla">UrlIsFileUrl</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisnohistorya">UrlIsNoHistory</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisopaquea">UrlIsOpaque</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines UrlIs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
