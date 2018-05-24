---
UID: NF:wininet.InternetGetCookieExA
title: InternetGetCookieExA function
author: windows-driver-content
description: Retrieves data stored in cookies associated with a specified URL.
old-location: wininet\internetgetcookieex.htm
old-project: WinInet
ms.assetid: 5006f009-e217-4fdc-9e4e-800ff5fcbf03
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: INTERNET_COOKIE_HTTPONLY, INTERNET_COOKIE_THIRD_PARTY, INTERNET_FLAG_RESTRICTED_ZONE, InternetGetCookieEx, InternetGetCookieEx function [WinINet], InternetGetCookieExA, InternetGetCookieExW, wininet.internetgetcookieex, wininet/InternetGetCookieEx, wininet/InternetGetCookieExA, wininet/InternetGetCookieExW
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
req.unicode-ansi: InternetGetCookieExW (Unicode) and InternetGetCookieExA (ANSI)
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
-	InternetGetCookieEx
-	InternetGetCookieExA
-	InternetGetCookieExW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetGetCookieExA function


## -description


The <b>InternetGetCookieEx</b> function retrieves data stored in cookies associated with a specified URL. Unlike <a href="https://msdn.microsoft.com/12c1ebab-3954-4995-9e1f-bf29699af396">InternetGetCookie</a>, <b>InternetGetCookieEx</b> can be used to  restrict data retrieved to a single cookie name or, by policy, associated with untrusted sites or third-party cookies.


## -parameters




### -param lpszUrl

TBD


### -param lpszCookieName [in]

A pointer to a <b>null</b>-terminated string that contains the name of the cookie to retrieve. This name is case-sensitive.


### -param lpszCookieData [in, out, optional]

A pointer to a buffer to receive the cookie data.


### -param lpdwSize [in, out]

A pointer to a DWORD variable. 

On entry, the variable must contain the size, in TCHARs, of the buffer pointed to by the <i>pchCookieData</i> parameter.

On exit, if the function is successful, this variable contains the number of TCHARs of cookie data copied into the buffer. If <b>NULL</b> was passed as the <i>lpszCookieData</i> parameter, or if the function fails with an error of <b>ERROR_INSUFFICIENT_BUFFER</b>, the variable contains the size, in BYTEs, of buffer required to receive the cookie data.

This parameter cannot be <b>NULL</b> or <b>InternetGetCookieEx</b> fails and returns an  <b>ERROR_INVALID_PARAMETER</b> error.


### -param dwFlags [in]

A flag that controls how the function retrieves cookie data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_HTTPONLY"></a><a id="internet_cookie_httponly"></a><dl>
<dt><b>INTERNET_COOKIE_HTTPONLY</b></dt>
</dl>
</td>
<td width="60%">
Enables the retrieval of cookies that are marked as "HTTPOnly".  



Do  not use this flag if you expose a scriptable interface, because this has security implications. It is imperative that you use this flag only if you can guarantee that you will never expose the cookie to third-party code by way of an extensibility mechanism you provide.


<b>Version:  </b>Requires Internet Explorer 8.0 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_THIRD_PARTY"></a><a id="internet_cookie_third_party"></a><dl>
<dt><b>INTERNET_COOKIE_THIRD_PARTY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves only third-party cookies if policy explicitly allows all cookies for the specified URL to be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_RESTRICTED_ZONE"></a><a id="internet_flag_restricted_zone"></a><dl>
<dt><b>INTERNET_FLAG_RESTRICTED_ZONE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves only cookies that would be allowed if the specified URL were untrusted; that is, if it belonged to the URLZONE_UNTRUSTED zone.

</td>
</tr>
</table>
 


### -param lpReserved [in]

Reserved for future use. Set to <b>NULL</b>.


#### - lpszURL [in]

A pointer to a <b>null</b>-terminated string that contains the URL with which the cookie to retrieve is associated. This parameter cannot be <b>NULL</b> or <b>InternetGetCookieEx</b> fails and returns an  <b>ERROR_INVALID_PARAMETER</b> error.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get a specific error value, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If <b>NULL</b> is passed to <i>lpszCookieData</i>, the call will succeed and the function will not set <b>ERROR_INSUFFICIENT_BUFFER</b>.


The following error codes may be set by this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Returned if cookie data retrieved is larger than the buffer size pointed to by the <i>pcchCookieData</i> parameter or if that parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Returned if either the  <i>pchURL</i> or the <i>pcchCookieData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Returned if no cookied data as specified could be retrieved.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c3574592-572f-4fde-adfa-aed3e862f13f">HTTP Cookies</a>



<a href="https://msdn.microsoft.com/12c1ebab-3954-4995-9e1f-bf29699af396">InternetGetCookie</a>



<a href="https://msdn.microsoft.com/1b1ca72e-9c74-4e94-86a9-6fee12c83933">InternetSetCookie</a>



<a href="https://msdn.microsoft.com/5044761f-152d-4606-87d2-c56a11db18c4">InternetSetCookieEx</a>



<a href="https://msdn.microsoft.com/c00279cf-9cdc-4caf-8549-af1851edfa25">Managing Cookies</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

