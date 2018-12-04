---
UID: NF:shlwapi.UrlIsOpaqueW
title: UrlIsOpaqueW function
author: windows-sdk-content
description: Returns whether a URL is opaque.
old-location: shell\UrlIsOpaque.htm
tech.root: shell
ms.assetid: 460f4d41-2796-496d-9199-f2d1cd6e4a24
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: UrlIsOpaque, UrlIsOpaque function [Windows Shell], UrlIsOpaqueA, UrlIsOpaqueW, _win32_UrlIsOpaque, shell.UrlIsOpaque, shlwapi/UrlIsOpaque, shlwapi/UrlIsOpaqueA, shlwapi/UrlIsOpaqueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsOpaqueW (Unicode) and UrlIsOpaqueA (ANSI)
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
api_name:
 - UrlIsOpaque
 - UrlIsOpaqueA
 - UrlIsOpaqueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UrlIsOpaqueW function


## -description


Returns whether a URL is opaque.


## -parameters




### -param pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


## -returns



Type: <b>BOOL</b>

Returns a nonzero value if the URL is opaque, or zero otherwise.




## -remarks



A URL that has a scheme that is not followed by two slashes (//) is opaque. For example, mailto:xyz@litwareinc.com is an opaque URL. Opaque URLs cannot be separated into the standard URL hierarchy. <b>UrlIsOpaque</b> is equivalent to the following:

				

<pre class="syntax" xml:space="preserve"><code>UrlIs(pszURL, URLIS_OPAQUE)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2e83c953-b4c5-4411-90ca-49ffb94ee374">UrlIs</a>
 

 

