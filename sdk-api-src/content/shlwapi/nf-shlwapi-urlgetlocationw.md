---
UID: NF:shlwapi.UrlGetLocationW
title: UrlGetLocationW function
author: windows-sdk-content
description: Retrieves the location from a URL.
old-location: shell\UrlGetLocation.htm
old-project: shell
ms.assetid: e75bde92-2ca0-4d34-a276-50b4eeceda1c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UrlGetLocation, UrlGetLocation function [Windows Shell], UrlGetLocationA, UrlGetLocationW, _win32_UrlGetLocation, shell.UrlGetLocation, shlwapi/UrlGetLocation, shlwapi/UrlGetLocationA, shlwapi/UrlGetLocationW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: URL_SCHEME
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
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
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



