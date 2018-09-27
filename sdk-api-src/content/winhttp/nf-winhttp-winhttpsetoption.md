---
UID: NF:winhttp.WinHttpSetOption
title: WinHttpSetOption function
author: windows-sdk-content
description: The WinHttpSetOption function sets an Internet option.
old-location: http\winhttpsetoption.htm
tech.root: winhttp
ms.assetid: bcf1da09-5787-4d2a-82ae-6965e27fa477
ms.author: windowssdkdev
ms.date: 09/11/2018
ms.keywords: WinHttpSetOption, WinHttpSetOption function [WinHTTP], http.winhttpsetoption, winhttp.winhttpsetoption_function, winhttp/WinHttpSetOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpSetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
---

# WinHttpSetOption function


## -description


The <b>WinHttpSetOption</b> function sets an Internet option.


## -parameters




### -param hInternet [in]

The <a href="https://msdn.microsoft.com/0bd82860-1347-40c8-ae77-c4d865c109be">HINTERNET</a> handle on which to set data. Be aware  that this can be either a Session handle or a Request handle, depending on what option is being set. For more information about how to determine which handle is appropriate to use in setting a particular option, see the  <a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a>.


### -param dwOption [in]

An unsigned long integer value that contains the Internet option to set. This can be one of the 
<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a> values.


### -param lpBuffer [in]

A pointer to a buffer that contains the option setting.


### -param dwBufferLength [in]

Unsigned long integer value that contains the length of the 
<i>lpBuffer</i> buffer. The length of the buffer is specified in characters for the following options; for all other options, the length is specified in bytes.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be carried out because the handle supplied is not in the correct state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_OPTION</b></dt>
</dl>
</td>
<td width="60%">
A request to 
<a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> or 
<a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> specified an invalid option value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid.

This value will be returned if <b>WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL</b> is set to a value lower than 15000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPTION_NOT_SETTABLE</b></dt>
</dl>
</td>
<td width="60%">
The requested option cannot be set, only queried.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid.

This value will be returned if <b>WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL</b> is set to a value lower than 15000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>
 




## -remarks



Credentials passed to <b>WinHttpSetOption</b> could be unexpectedly sent in plaintext. It is  strongly recommended that you  use <a href="https://msdn.microsoft.com/37fb9342-c5c2-46a3-a8b0-83060aa997e2">WinHttpQueryAuthSchemes</a>  and <a href="https://msdn.microsoft.com/a864c708-9481-460a-87aa-1d31c344c0a1">WinHttpSetCredentials</a> instead of <b>WinHttpSetOption</b> for setting credentials.

<div class="alert"><b>Note</b>  When using Passport authentication, however, a WinHTTP application responding to a 407 status code must use <b>WinHttpSetOption</b> to provide proxy credentials rather than <a href="https://msdn.microsoft.com/a864c708-9481-460a-87aa-1d31c344c0a1">WinHttpSetCredentials</a>. This is only true when using Passport authentication; in all other circumstances,  use <b>WinHttpSetCredentials</b>.</div>
<div> </div>
Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the error ERROR_INVALID_PARAMETER if an option flag is specified that cannot be set.

For more information and code examples that show the use of <b>WinHttpSetOption</b>, see <a href="https://msdn.microsoft.com/077d6275-8600-4091-b78e-419a41a2101a">Authentication in WinHTTP</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/077d6275-8600-4091-b78e-419a41a2101a">Authentication in WinHTTP</a>



<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>



<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>



<a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a>
 

 

