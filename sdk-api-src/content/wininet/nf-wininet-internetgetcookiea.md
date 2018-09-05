---
UID: NF:wininet.InternetGetCookieA
title: InternetGetCookieA function
author: windows-sdk-content
description: Retrieves the cookie for the specified URL.
old-location: wininet\internetgetcookie.htm
old-project: WinInet
ms.assetid: 12c1ebab-3954-4995-9e1f-bf29699af396
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InternetGetCookie, InternetGetCookie function [WinINet], InternetGetCookieA, InternetGetCookieW, _win32_internetgetcookie, wininet.internetgetcookie, wininet/InternetGetCookie, wininet/InternetGetCookieA, wininet/InternetGetCookieW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetCookieW (Unicode) and InternetGetCookieA (ANSI)
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
 - InternetGetCookie
 - InternetGetCookieA
 - InternetGetCookieW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetGetCookieA function


## -description


Retrieves the cookie for the specified URL.


## -parameters




### -param lpszUrl [in]

A pointer to a <b>null</b>-terminated string that specifies the URL for which cookies are to be retrieved.


### -param lpszCookieName [in]

Not implemented.


### -param lpszCookieData [out]

A pointer to a buffer that receives the cookie data. This parameter can be <b>NULL</b>.


### -param lpdwSize [in, out]

A pointer to a variable that specifies the size of the 
<i>lpszCookieData</i> parameter buffer, in TCHARs. If the function succeeds, the buffer receives the amount of data copied to the 
<i>lpszCookieData</i> buffer. If 
<i>lpszCookieData</i> is <b>NULL</b>, this parameter receives a value that specifies the size of the buffer necessary to copy all the cookie data, expressed as a byte count.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error data, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error values apply to 
<b>InternetGetCookie</b>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There is no cookie for the specified URL and all its parents.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The value passed in 
<i>lpdwSize</i> is insufficient to copy all the cookie data. The value returned in 
<i>lpdwSize</i> is the size of the buffer necessary to get all the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is invalid.

The <i>lpszUrl</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>InternetGetCookie</b> does not require a call to 
<a href="https://msdn.microsoft.com/9ec087c9-d484-4763-a527-2ea5c1a0cf28">InternetOpen</a>. 
<b>InternetGetCookie</b> checks in the windows\cookies directory for persistent cookies that have an expiration date set sometime in the future. 
<b>InternetGetCookie</b> also searches memory for any session cookies, that is, cookies that do not have an expiration date that were created in the same process by 
<a href="https://msdn.microsoft.com/1b1ca72e-9c74-4e94-86a9-6fee12c83933">InternetSetCookie</a>, because these cookies are not written to any files. Rules for creating cookie files are internal to the system and can change in the future.

				As noted in <a href="https://msdn.microsoft.com/c3574592-572f-4fde-adfa-aed3e862f13f">HTTP Cookies</a>, <b>InternetGetCookie</b> does not return cookies that the server marked as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c3574592-572f-4fde-adfa-aed3e862f13f">HTTP Cookies</a>



<a href="https://msdn.microsoft.com/5006f009-e217-4fdc-9e4e-800ff5fcbf03">InternetGetCookieEx</a>



<a href="https://msdn.microsoft.com/1b1ca72e-9c74-4e94-86a9-6fee12c83933">InternetSetCookie</a>



<a href="https://msdn.microsoft.com/5044761f-152d-4606-87d2-c56a11db18c4">InternetSetCookieEx</a>



<a href="https://msdn.microsoft.com/c00279cf-9cdc-4caf-8549-af1851edfa25">Managing Cookies</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

