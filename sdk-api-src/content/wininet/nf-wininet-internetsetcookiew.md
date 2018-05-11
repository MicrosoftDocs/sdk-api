---
UID: NF:wininet.InternetSetCookieW
title: InternetSetCookieW function
author: windows-driver-content
description: Creates a cookie associated with the specified URL.
old-location: wininet\internetsetcookie.htm
old-project: WinInet
ms.assetid: 1b1ca72e-9c74-4e94-86a9-6fee12c83933
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: InternetSetCookie, InternetSetCookie function [WinINet], InternetSetCookieA, InternetSetCookieW, _win32_internetsetcookie, wininet.internetsetcookie, wininet/InternetSetCookie, wininet/InternetSetCookieA, wininet/InternetSetCookieW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetCookieW (Unicode) and InternetSetCookieA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	InternetSetCookie
-	InternetSetCookieA
-	InternetSetCookieW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetSetCookieW function


## -description


Creates a cookie associated with the specified URL.


## -parameters




### -param lpszUrl [in]

Pointer to a <b>null</b>-terminated string that specifies the URL for which the cookie should be set.


### -param lpszCookieName [in]

Pointer to a <b>null</b>-terminated string that specifies the name to be associated with the cookie data. If this parameter is <b>NULL</b>, no name is associated with the cookie.


### -param lpszCookieData [in]

Pointer to the actual data to be associated with the URL.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Cookies created by 
<b>InternetSetCookie</b> without an expiration date are stored in memory and are available only in the same process that created them. Cookies that include an expiration date are stored in the windows\cookies directory.

Creating a new cookie might cause a dialog box to appear on the screen asking the user if they want to allow or disallow  cookies from this site based on the privacy settings for the user.


<div class="alert"><b>Caution</b>  <b>InternetSetCookie</b> will unconditionally create a cookie even if “Block all cookies” is set in Internet Explorer. This behavior can be viewed as a breach of privacy even though such cookies are not subsequently sent back to servers while the “Block all cookies” setting is active. Applications should use <a href="https://msdn.microsoft.com/5044761f-152d-4606-87d2-c56a11db18c4">InternetSetCookieEx</a> to correctly honor the user's privacy settings.

<p class="note">For more cookie internals, see <a href="http://go.microsoft.com/fwlink/p/?linkid=186361">http://blogs.msdn.com/ieinternals/archive/2009/08/20/WinINET-IE-Cookie-Internals-FAQ.aspx</a>.

</div>
<div> </div>


Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c3574592-572f-4fde-adfa-aed3e862f13f">HTTP Cookies</a>



<a href="https://msdn.microsoft.com/12c1ebab-3954-4995-9e1f-bf29699af396">InternetGetCookie</a>



<a href="https://msdn.microsoft.com/5006f009-e217-4fdc-9e4e-800ff5fcbf03">InternetGetCookieEx</a>



<a href="https://msdn.microsoft.com/5044761f-152d-4606-87d2-c56a11db18c4">InternetSetCookieEx</a>



<a href="https://msdn.microsoft.com/c00279cf-9cdc-4caf-8549-af1851edfa25">Managing Cookies</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

