---
UID: NF:wininet.InternetTimeToSystemTime
title: InternetTimeToSystemTime function
author: windows-sdk-content
description: Converts an HTTP time/date string to a SYSTEMTIME structure.
old-location: wininet\internettimetosystemtime.htm
tech.root: WinInet
ms.assetid: fcfe99de-13b2-4e93-a978-f013ddae89f0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InternetTimeToSystemTime, InternetTimeToSystemTime function [WinINet], InternetTimeToSystemTimeA, InternetTimeToSystemTimeW, _inet_internettimetosystemtime_function, wininet.internettimetosystemtime, wininet/InternetTimeToSystemTime, wininet/InternetTimeToSystemTimeA, wininet/InternetTimeToSystemTimeW
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
req.unicode-ansi: InternetTimeToSystemTimeW (Unicode) and InternetTimeToSystemTimeA (ANSI)
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
 - InternetTimeToSystemTime
 - InternetTimeToSystemTimeA
 - InternetTimeToSystemTimeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetTimeToSystemTime function


## -description


Converts an HTTP time/date string to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


## -parameters




### -param lpszTime [in]

Pointer to a null-terminated string that specifies the date/time to  be converted.


### -param pst [out]

Pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the converted time.


### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if the string was converted, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

