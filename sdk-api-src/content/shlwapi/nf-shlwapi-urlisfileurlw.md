---
UID: NF:shlwapi.UrlIsFileUrlW
title: UrlIsFileUrlW macro
author: windows-sdk-content
description: Tests a URL to determine if it is a file URL.
old-location: shell\UrlIsFileUrl.htm
tech.root: shell
ms.assetid: b122d3e4-47cc-47c0-a30c-6f9d1aa9d174
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: UrlIsFileUrl, UrlIsFileUrl function [Windows Shell], UrlIsFileUrlA, UrlIsFileUrlW, _win32_UrlIsFileUrl, shell.UrlIsFileUrl, shlwapi/UrlIsFileUrl, shlwapi/UrlIsFileUrlA, shlwapi/UrlIsFileUrlW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsFileUrlW (Unicode) and UrlIsFileUrlA (ANSI)
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
api_name:
 - UrlIsFileUrl
 - UrlIsFileUrlA
 - UrlIsFileUrlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UrlIsFileUrlW macro


## -description


Tests a URL to determine if it is a file URL.


## -parameters




### -param pszURL

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the URL.


## -remarks



A file URL has the form "File://
				<i>xxx</i>". <b>UrlIsFileUrl</b> is actually one of the following macros, depending on whether ANSI or Unicode is selected.
				


```

#define  UrlIsFileUrlA(pszURL) UrlIsA(pszURL, URLIS_FILEURL)
#define  UrlIsFileUrlW(pszURL) UrlIsW(pszURL, URLIS_FILEURL)
				
```





## -see-also




<a href="https://msdn.microsoft.com/2e83c953-b4c5-4411-90ca-49ffb94ee374">UrlIs</a>
 

 

