---
UID: NF:wininet.InternetGetLastResponseInfoA
title: InternetGetLastResponseInfoA function
author: windows-sdk-content
description: Retrieves the last error description or server response on the thread calling this function.
old-location: wininet\internetgetlastresponseinfo.htm
old-project: WinInet
ms.assetid: 0aa274c5-0aa0-4eb9-8aef-3128e735759d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InternetGetLastResponseInfo, InternetGetLastResponseInfo function [WinINet], InternetGetLastResponseInfoA, InternetGetLastResponseInfoW, _win32_internetgetlastresponseinfo, wininet.internetgetlastresponseinfo, wininet/InternetGetLastResponseInfo, wininet/InternetGetLastResponseInfoA, wininet/InternetGetLastResponseInfoW
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
req.unicode-ansi: InternetGetLastResponseInfoW (Unicode) and InternetGetLastResponseInfoA (ANSI)
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
 - InternetGetLastResponseInfo
 - InternetGetLastResponseInfoA
 - InternetGetLastResponseInfoW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetGetLastResponseInfoA function


## -description


Retrieves the last error description or server response on the thread calling this function.


## -parameters




### -param lpdwError [out]

Pointer to a variable that receives an error message pertaining to the operation that failed.


### -param lpszBuffer [out]

Pointer to a buffer that receives the error text.


### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the size of the 
<i>lpszBuffer</i> buffer, in <b>TCHARs</b>. When the function returns, this parameter contains the size of the string written to the buffer, not including the terminating zero.


## -returns



Returns <b>TRUE</b> if error text was successfully written to the buffer, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the buffer is too small to hold all the error text, 
<b>GetLastError</b> returns <b>ERROR_INSUFFICIENT_BUFFER</b>, and the 
<i>lpdwBufferLength</i> parameter contains the minimum buffer size required to return all the error text.




## -remarks



The FTP protocols can return additional text information along with most errors. This extended error information can be retrieved by using the 
<b>InternetGetLastResponseInfo</b> function whenever 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
<a href="https://msdn.microsoft.com/338bf65f-ebe5-4434-8407-9ab2a4c8d381">ERROR_INTERNET_EXTENDED_ERROR</a> (occurring after an unsuccessful function call).

The buffer pointed to by 
<i>lpszBuffer</i> must be large enough to hold both the error string and a zero terminator at the end of the string. However, note that the value returned in 
<i>lpdwBufferLength</i> does not include the terminating zero.

<b>InternetGetLastResponseInfo</b> can be called multiple times until another function is called on this thread. When another function is called, the internal buffer that is storing the last response information is cleared.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

