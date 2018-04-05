---
UID: NF:winhttp.WinHttpTimeToSystemTime
title: WinHttpTimeToSystemTime function
author: windows-driver-content
description: The WinHttpTimeToSystemTime function takes an HTTP time/date string and converts it to a SYSTEMTIME structure.
old-location: http\winhttptimetosystemtime.htm
old-project: WinHttp
ms.assetid: 4a587832-e1ce-42d4-97bb-a728f895906b
ms.author: windowsdriverdev
ms.date: 3/8/2018
ms.keywords: WinHttpTimeToSystemTime, WinHttpTimeToSystemTime function [WinHTTP], http.winhttptimetosystemtime, winhttp.winhttptimetosystemtime_function, winhttp/WinHttpTimeToSystemTime
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
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winhttp.dll
api_name:
-	WinHttpTimeToSystemTime
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpTimeToSystemTime function


## -description


The <b>WinHttpTimeToSystemTime</b> function takes an HTTP time/date string and converts it to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


## -parameters




### -param pwszTime [in]

Pointer to a null-terminated date/time string to convert. This value must use the format defined in section 3.3 of the <a href="http://www.ietf.org/rfc/rfc2616.txt">RFC2616</a>.


### -param pst [out]

Pointer to the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the converted time. 


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned is:

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

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows how to convert an HTTP formatted date to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    SYSTEMTIME  sTime;
    LPCWSTR     pwszTimeStr = L"Tue, 21 Nov 2000 01:06:53 GMT";

    // Convert the HTTP string to a SYSTEMTIME structure.
    if (!WinHttpTimeToSystemTime( pwszTimeStr, &amp;sTime))
    {
        printf( "Error %u in WinHttpTimeToSystemTime.\n", GetLastError());
    }
    else
    {
        // Print the date.
        printf( "The U.S. formatted date is (%u/%u/%u)\n", 
                sTime.wMonth, sTime.wDay, sTime.wYear);
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8337f699-3ec0-4397-acc2-6dc813f7542d">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>



<a href="https://msdn.microsoft.com/8d55e3bb-0b86-41d9-ba39-62feb2acc707">WinHttpTimeFromSystemTime</a>
 

 

