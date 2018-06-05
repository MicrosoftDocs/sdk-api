---
UID: NF:winhttp.WinHttpQueryOption
title: WinHttpQueryOption function
author: windows-sdk-content
description: The WinHttpQueryOption function queries an Internet option on the specified handle.
old-location: http\winhttpqueryoption.htm
old-project: WinHttp
ms.assetid: 47973eab-de70-47bf-9713-97b87a500cfa
ms.author: windowssdkdev
ms.date: 03/08/2018
ms.keywords: WinHttpQueryOption, WinHttpQueryOption function [WinHTTP], http.winhttpqueryoption, winhttp.winhttpqueryoption_function, winhttp/WinHttpQueryOption
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winhttp.dll
api_name:
-	WinHttpQueryOption
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpQueryOption function


## -description


The <b>WinHttpQueryOption</b> function queries an Internet option on the specified handle.


## -parameters




### -param hInternet [in]

An <b>HINTERNET</b> handle on which to query information. Note that this can be either a Session handle or a Request handle, depending on what option is being queried; see the  <a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a> topic to determine which handle is appropriate to use in querying a particular option.


### -param dwOption [in]

An unsigned long integer value that contains the Internet option to query. This can be one of the 
<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a> values.


### -param lpBuffer [out]

A pointer to a buffer that receives the option setting. Strings returned by the 
<b>WinHttpQueryOption</b> function are globally allocated, so the calling application must globally free the string when it finishes using it. Setting this parameter to <b>NULL</b> causes this function to return <b>FALSE</b>.  Calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> then returns ERROR_INSUFFICIENT_BUFFER and 
<i>lpdwBufferLength</i>          contains the number of bytes required to hold the requested information.


### -param lpdwBufferLength [in, out]

A pointer to an unsigned long integer variable that contains the length of 
<i>lpBuffer</i>, in bytes. When the function returns, the variable receives the length of the data placed into 
<i>lpBuffer</i>. If 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter receives the number of bytes required to hold the requested information.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following.

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
An invalid option value was specified.

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



Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the ERROR_INVALID_PARAMETER if an option flag that is invalid for the specified handle type is passed to the 
<i>dwOption</i> parameter.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example demonstrates retrieving the connection 
                time-out value:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    DWORD data;
    DWORD dwSize = sizeof(DWORD);

    // Use WinHttpOpen to obtain an HINTERNET handle.
    HINTERNET hSession = WinHttpOpen(L"A WinHTTP Example Program/1.0", 
                                    WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                                    WINHTTP_NO_PROXY_NAME, 
                                    WINHTTP_NO_PROXY_BYPASS, 0);
    if (hSession)
    {


        // Use WinHttpQueryOption to retrieve internet options.
        if (WinHttpQueryOption( hSession, 
                                WINHTTP_OPTION_CONNECT_TIMEOUT, 
                                &amp;data, &amp;dwSize))
        {
            printf("Connection timeout: %u ms\n\n",data);
        }
        else
        {
            printf( "Error %u in WinHttpQueryOption.\n", GetLastError());
        }        
        
        // When finished, release the HINTERNET handle.
        WinHttpCloseHandle(hSession);
    }
    else
    {
        printf("Error %u in WinHttpOpen.\n", GetLastError());
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>



<a href="https://msdn.microsoft.com/afcdad8d-687e-4a1f-99d8-5d8be13825fa">WinHttpConnect</a>



<a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>



<a href="https://msdn.microsoft.com/9ecd035d-1abf-48ca-baf2-d9754f912c60">WinHttpOpenRequest</a>
 

 

