---
UID: NF:wininet.InternetGoOnlineA
title: InternetGoOnlineA function
author: windows-sdk-content
description: Prompts the user for permission to initiate connection to a URL.
old-location: wininet\internetgoonline.htm
old-project: WinInet
ms.assetid: ed1c0282-5469-49d5-8a8c-b7671d27ebd2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INTERNET_GOONLINE_REFRESH, InternetGoOnline, InternetGoOnline function [WinINet], InternetGoOnlineA, InternetGoOnlineW, _inet_internetgoonline_function, wininet.internetgoonline, winineti/InternetGoOnline, winineti/InternetGoOnlineA, winineti/InternetGoOnlineW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: Wininet.h, Winineti.h, Wininet.h, Winineti.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGoOnlineW (Unicode) and InternetGoOnlineA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetGoOnline
 - InternetGoOnlineA
 - InternetGoOnlineW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetGoOnlineA function


## -description


Prompts the user for permission to initiate connection to a URL.


## -parameters




### -param lpszURL [in]

Pointer to a null-terminated string that specifies the URL of the website for the connection.


### -param hwndParent [in]

Handle to the parent window.


### -param dwFlags [in]

This parameter can be zero or the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_GOONLINE_REFRESH"></a><a id="internet_goonline_refresh"></a><dl>
<dt><b>INTERNET_GOONLINE_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. Applications can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code.

If the functions fails, it can  return the following error code:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is incorrect.

The <i>dwFlags</i> parameter contains a value other than zero or <b>INTERNET_GOONLINE_REFRESH</b>.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dd33ed4b-eb7c-449c-b309-8f5c290a5a93">Establishing a Dial-Up Connection to the Internet</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

