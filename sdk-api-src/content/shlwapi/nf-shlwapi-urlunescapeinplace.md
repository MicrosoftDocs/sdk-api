---
UID: NF:shlwapi.UrlUnescapeInPlace
title: UrlUnescapeInPlace macro
author: windows-sdk-content
description: Converts escape sequences back into ordinary characters and overwrites the original string.
old-location: shell\UrlUnescapeInPlace.htm
old-project: shell
ms.assetid: 315215dc-c074-4abb-8bb2-006eff18b88d
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: URL_DONT_UNESCAPE_EXTRA_INFO, UrlUnescapeInPlace, UrlUnescapeInPlace function [Windows Shell], _win32_UrlUnescapeInPlace, shell.UrlUnescapeInPlace, shlwapi/UrlUnescapeInPlace
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - UrlUnescapeInPlace
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlUnescapeInPlace macro


## -description


Converts escape sequences back into ordinary characters and overwrites the original string.


## -parameters




### -param pszUrl

TBD


### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that control which characters are unescaped.



#### URL_DONT_UNESCAPE_EXTRA_INFO

Do not convert the # or ? character, or any characters following them in the string.


#### - pszURL [in, out]

Type: <b>LPTSTR</b>

A pointer to a <b>null</b>-terminated string that contains the URL. The converted string is returned through this parameter.


## -remarks



<b>UrlUnescapeInPlace</b> is equivalent to the following:
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UrlUnescape(pszUrl, NULL, NULL, dwFlags | URL_UNESCAPE_INPLACE)
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5bff5161-3b57-4f12-b126-42eac3f60267">UrlUnescape</a>
 

 

