---
UID: NF:shlwapi.UrlGetLocationW
title: UrlGetLocationW function (shlwapi.h)
description: Retrieves the location from a URL.
old-location: shell\UrlGetLocation.htm
tech.root: shell
ms.assetid: e75bde92-2ca0-4d34-a276-50b4eeceda1c
ms.date: 12/05/2018
ms.keywords: UrlGetLocation, UrlGetLocation function [Windows Shell], UrlGetLocationA, UrlGetLocationW, _win32_UrlGetLocation, shell.UrlGetLocation, shlwapi/UrlGetLocation, shlwapi/UrlGetLocationA, shlwapi/UrlGetLocationW
ms.topic: function
f1_keywords:
- shlwapi/UrlGetLocation
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlGetLocationW (Unicode) and UrlGetLocationA (ANSI)
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
- API-MS-Win-Core-url-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
- UrlGetLocation
- UrlGetLocationA
- UrlGetLocationW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UrlGetLocationW function


## -description


Retrieves the location from a URL.


## -parameters




### -param pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the location.


## -returns



Type: <b>LPCTSTR</b>

Returns a pointer to a null-terminated string with the location, or <b>NULL</b> otherwise.




## -remarks



The location is the segment of the URL starting with a ? or # character. If a file URL has a query string, the returned string includes the query string.



