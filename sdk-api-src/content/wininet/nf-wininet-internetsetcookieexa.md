---
UID: NF:wininet.InternetSetCookieExA
title: InternetSetCookieExA function
author: windows-sdk-content
description: The InternetSetCookieEx function creates a cookie with a specified name that is associated with a specified URL. This function differs from the InternetSetCookie function by being able to create third-party cookies.
old-location: wininet\internetsetcookieex.htm
tech.root: WinInet
ms.assetid: 5044761f-152d-4606-87d2-c56a11db18c4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INTERNET_COOKIE_EVALUATE_P3P, INTERNET_COOKIE_HTTPONLY, INTERNET_COOKIE_THIRD_PARTY, INTERNET_FLAG_RESTRICTED_ZONE, InternetSetCookieEx, InternetSetCookieEx function [WinINet], InternetSetCookieExA, InternetSetCookieExW, wininet.internetsetcookieex, wininet/InternetSetCookieEx, wininet/InternetSetCookieExA, wininet/InternetSetCookieExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetCookieExW (Unicode) and InternetSetCookieExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetCookieEx
 - InternetSetCookieExA
 - InternetSetCookieExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetSetCookieExA function


## -description


The <b>InternetSetCookieEx</b> function 
	      creates a cookie with a specified name that is associated with a specified URL. This function differs from 
	      the <a href="https://msdn.microsoft.com/1b1ca72e-9c74-4e94-86a9-6fee12c83933">InternetSetCookie</a> function by being able 
	      to create third-party cookies.


## -parameters




### -param lpszUrl [in]

Pointer to a <b>null</b>-terminated string that contains the URL for which the cookie should be set. 

If this pointer is <b>NULL</b>, <b>InternetSetCookieEx</b> fails with an <b>ERROR_INVALID_PARAMETER</b> error.


### -param lpszCookieName [in]

Pointer to a <b>null</b>-terminated string that  contains the name to associate with this cookie.
      If this pointer is <b>NULL</b>, then no name is associated with the cookie.


### -param lpszCookieData [in]

Pointer to a <b>null</b>-terminated string that contains the data to be associated with the new cookie.

If this pointer is <b>NULL</b>, <b>InternetSetCookieEx</b> fails with an <b>ERROR_INVALID_PARAMETER</b> error.


### -param dwFlags [in]

Flags that control how the function retrieves cookie data:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_EVALUATE_P3P"></a><a id="internet_cookie_evaluate_p3p"></a><dl>
<dt><b>INTERNET_COOKIE_EVALUATE_P3P</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set and the <i>dwReserved</i> parameter is not <b>NULL</b>, then the <i>dwReserved</i> parameter is cast to an <b>LPCTSTR</b> that points to a Platform-for-Privacy-Protection (P3P) header for the cookie in question.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_HTTPONLY"></a><a id="internet_cookie_httponly"></a><dl>
<dt><b>INTERNET_COOKIE_HTTPONLY</b></dt>
</dl>
</td>
<td width="60%">
Enables the retrieval of cookies that are marked as "HTTPOnly".  



Do  not use this flag if you expose a scriptable interface, because this has security implications. If you expose a scriptable interface, you can become an attack vector for cross-site scripting attacks.  It is utterly imperative that you use this flag only if they can guarantee that you will never permit third-party code to set a cookie using this flag by way of an extensibility mechanism you provide.

 

<b>Version:  </b>Requires Internet Explorer 8.0 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_THIRD_PARTY"></a><a id="internet_cookie_third_party"></a><dl>
<dt><b>INTERNET_COOKIE_THIRD_PARTY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the cookie being set is a third-party cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_RESTRICTED_ZONE"></a><a id="internet_flag_restricted_zone"></a><dl>
<dt><b>INTERNET_FLAG_RESTRICTED_ZONE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the cookie being set is associated with an untrusted site.

</td>
</tr>
</table>
 


### -param dwReserved [in]

<b>NULL</b>, or contains a pointer to a Platform-for-Privacy-Protection (P3P) header to be associated with the cookie.


## -returns



Returns a member of the <a href="https://msdn.microsoft.com/3f43f492-3133-4cbd-9ab9-3c9600ef5263">InternetCookieState</a> enumeration if successful,  or  <b>FALSE</b> if the function fails. On failure, if a call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_NOT_ENOUGH_MEMORY,  insufficient system memory was available.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c3574592-572f-4fde-adfa-aed3e862f13f">HTTP Cookies</a>



<a href="https://msdn.microsoft.com/12c1ebab-3954-4995-9e1f-bf29699af396">InternetGetCookie</a>



<a href="https://msdn.microsoft.com/5006f009-e217-4fdc-9e4e-800ff5fcbf03">InternetGetCookieEx</a>



<a href="https://msdn.microsoft.com/1b1ca72e-9c74-4e94-86a9-6fee12c83933">InternetSetCookie</a>



<a href="https://msdn.microsoft.com/c00279cf-9cdc-4caf-8549-af1851edfa25">Managing Cookies</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

