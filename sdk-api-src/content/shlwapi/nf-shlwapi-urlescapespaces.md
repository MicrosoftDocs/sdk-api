---
UID: NF:shlwapi.UrlEscapeSpaces
title: UrlEscapeSpaces macro
author: windows-sdk-content
description: A macro that converts space characters into their corresponding escape sequence.
old-location: shell\UrlEscapeSpaces.htm
tech.root: Shell
ms.assetid: d6d676f1-0ef3-4701-99b2-ca520b39ce6e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: UrlEscapeSpaces, UrlEscapeSpaces function [Windows Shell], _win32_UrlEscapeSpaces, shell.UrlEscapeSpaces, shlwapi/UrlEscapeSpaces
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
req.unicode-ansi: 
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
 - UrlEscapeSpaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UrlEscapeSpaces macro


## -description


A macro that converts space characters into their corresponding escape sequence.


## -parameters




### -param pszUrl [in]

Type: <b>LPCTSTR</b>

A pointer to a URL string. If it does not refer to a file, it must include a valid scheme such as "http://".


### -param pszEscaped [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string containing the string pointed to by <i>pszURL</i>, with space characters converted to their escape sequence.


### -param pcchEscaped [out]

Type: <b>LPDWORD</b>

The number of characters in <i>pszEscaped</i>.


## -remarks



<b>UrlEscapeSpaces</b> is equivalent to the following: 

				


```

UrlCanonicalize(pszUrl, 
                pszEscaped, 
                pcchEscaped, 
                URL_ESCAPE_SPACES_ONLY | URL_DONT_ESCAPE_EXTRA_INFO )
				
```





## -see-also




<a href="https://msdn.microsoft.com/70802745-0611-4d37-800e-b50d5ea23426">UrlCanonicalize</a>
 

 

