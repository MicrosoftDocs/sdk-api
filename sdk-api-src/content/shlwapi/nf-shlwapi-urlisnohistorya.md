---
UID: NF:shlwapi.UrlIsNoHistoryA
title: UrlIsNoHistoryA function
author: windows-sdk-content
description: Returns whether a URL is a URL that browsers typically do not include in navigation history.
old-location: shell\UrlIsNoHistory.htm
old-project: shell
ms.assetid: 7602d2ef-1f21-4b2f-8ac9-195bb21d6ae7
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: UrlIsNoHistory, UrlIsNoHistory function [Windows Shell], UrlIsNoHistoryA, UrlIsNoHistoryW, _win32_UrlIsNoHistory, shell.UrlIsNoHistory, shlwapi/UrlIsNoHistory, shlwapi/UrlIsNoHistoryA, shlwapi/UrlIsNoHistoryW
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
req.unicode-ansi: UrlIsNoHistoryW (Unicode) and UrlIsNoHistoryA (ANSI)
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
api_name:
 - UrlIsNoHistory
 - UrlIsNoHistoryA
 - UrlIsNoHistoryW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlIsNoHistoryA function


## -description


Returns whether a URL is a URL that browsers typically do not include in navigation history.


## -parameters




### -param pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


## -returns



Type: <b>BOOL</b>

Returns a nonzero value if the URL is a URL that is not included in navigation history, or zero otherwise.




## -remarks



This function is equivalent to the following:
				
                

<pre class="syntax" xml:space="preserve"><code>UrlIs(pszURL, URLIS_NOHISTORY)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2e83c953-b4c5-4411-90ca-49ffb94ee374">UrlIs</a>
 

 

