---
UID: NF:wininet.InternetTimeFromSystemTimeA
title: InternetTimeFromSystemTimeA function (wininet.h)
author: windows-sdk-content
description: Formats a date and time according to the HTTP version 1.0 specification.
old-location: wininet\internettimefromsystemtime.htm
tech.root: wininet
ms.assetid: b52ba402-bad1-4005-b9d0-7630194272d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetTimeFromSystemTime, InternetTimeFromSystemTime function [WinINet], InternetTimeFromSystemTimeA, InternetTimeFromSystemTimeW, _inet_internettimefromsystemtime_function, wininet.internettimefromsystemtime, wininet/InternetTimeFromSystemTime, wininet/InternetTimeFromSystemTimeA, wininet/InternetTimeFromSystemTimeW
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetTimeFromSystemTimeW (Unicode) and InternetTimeFromSystemTimeA (ANSI)
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
 - API-MS-Win-Http-Time-l1-1-0.dll
 - KernelBase.dll
api_name:
 - InternetTimeFromSystemTime
 - InternetTimeFromSystemTimeA
 - InternetTimeFromSystemTimeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetTimeFromSystemTimeA function


## -description


Formats a date and time according to the HTTP version 1.0 specification.


## -parameters




### -param pst [in]

Pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date and time to format.


### -param dwRFC [in]

RFC format used. Currently, the only valid format is INTERNET_RFC1123_FORMAT.


### -param lpszTime [out]

Pointer to a string buffer that receives the formatted date and time. The buffer should be of size INTERNET_RFC1123_BUFSIZE.


### -param cbTime [in]

Size of the 
<i>lpszTime</i> buffer, in bytes.


## -returns



Returns TRUE if the function succeeds, or FALSE otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

