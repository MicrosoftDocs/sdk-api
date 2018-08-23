---
UID: NF:winhttp.WinHttpTimeFromSystemTime
title: WinHttpTimeFromSystemTime function
author: windows-sdk-content
description: Formats a date and time according to the HTTP version 1.0 specification.
old-location: http\winhttptimefromsystemtime.htm
old-project: winhttp
ms.assetid: 8d55e3bb-0b86-41d9-ba39-62feb2acc707
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: WinHttpTimeFromSystemTime, WinHttpTimeFromSystemTime function [WinHTTP], http.winhttptimefromsystemtime, winhttp.winhttptimefromsystemtime_function, winhttp/WinHttpTimeFromSystemTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpTimeFromSystemTime
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpTimeFromSystemTime function


## -description


The <b>WinHttpTimeFromSystemTime</b> function formats a date and time according to the HTTP version 1.0 specification.


## -parameters




### -param pst [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date and time to format.


### -param pwszTime [out]

A pointer to a string buffer that receives the formatted date and time. The buffer should equal to the size, in bytes, of WINHTTP_TIME_FORMAT_BUFSIZE.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get  extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Error codes include the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
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
</table>
 




## -remarks



Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="https://msdn.microsoft.com/34ce8f7d-7cc3-4b38-ba6a-1247f50ebd33">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHTTP Start Page.</div>
<div> </div>

#### Examples

The following  code example code shows how to convert a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure to a string that contains the time in HTTP format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    SYSTEMTIME  sTime;
    LPWSTR      pwszTimeStr;

    // Get the current time.
    GetSystemTime(&amp;sTime);

    // Allocate memory for the string.
    // Note: WINHTTP_TIME_FORMAT_BUFSIZE is a byte count.
    //       Therefore, you must divide the array by
    //       sizeof WCHAR to get the proper string length.
    pwszTimeStr = new WCHAR[WINHTTP_TIME_FORMAT_BUFSIZE/sizeof(WCHAR)];

    // Convert the current time to HTTP format.
    if(!WinHttpTimeFromSystemTime( &amp;sTime, pwszTimeStr))
    {
        printf( "Error %u in WinHttpTimeFromSystemTime.\n", GetLastError());
    }
    else
    {
        // Print the time.
        printf("Current time is (%S)\n", pwszTimeStr);
    }

    // Free the memory.
    delete [] pwszTimeStr;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/4a587832-e1ce-42d4-97bb-a728f895906b">WinHttpTimeToSystemTime</a>
 

 

