---
UID: NF:shlwapi.UrlIsFileUrlA
title: UrlIsFileUrlA macro
author: windows-sdk-content
description: Tests a URL to determine if it is a file URL.
old-location: shell\UrlIsFileUrl.htm
old-project: shell
ms.assetid: b122d3e4-47cc-47c0-a30c-6f9d1aa9d174
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UrlIsFileUrl, UrlIsFileUrl function [Windows Shell], UrlIsFileUrlA, UrlIsFileUrlW, _win32_UrlIsFileUrl, shell.UrlIsFileUrl, shlwapi/UrlIsFileUrl, shlwapi/UrlIsFileUrlA, shlwapi/UrlIsFileUrlW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: shlwapi.h
req.include-header: 
req.redist: 
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
 - UrlIsFileUrl
 - UrlIsFileUrlA
 - UrlIsFileUrlW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlIsFileUrlA macro


## -description


Tests a URL to determine if it is a file URL.


## -parameters




### -param pszURL

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the URL.


## -remarks



A file URL has the form "File://
				<i>xxx</i>". <b>UrlIsFileUrl</b> is actually one of the following macros, depending on whether ANSI or Unicode is selected.
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
#define  UrlIsFileUrlA(pszURL) UrlIsA(pszURL, URLIS_FILEURL)
#define  UrlIsFileUrlW(pszURL) UrlIsW(pszURL, URLIS_FILEURL)
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2e83c953-b4c5-4411-90ca-49ffb94ee374">UrlIs</a>
 

 

