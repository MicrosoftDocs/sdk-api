---
UID: NF:wininet.InternetReadFileExA
title: InternetReadFileExA function
author: windows-sdk-content
description: Reads data from a handle opened by the InternetOpenUrl or HttpOpenRequest function.
old-location: wininet\internetreadfileex.htm
tech.root: WinInet
ms.assetid: 04e7bb7e-d925-41fd-8333-3cb443a04c5b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InternetReadFileEx, InternetReadFileEx function [WinINet], InternetReadFileExA, InternetReadFileExW, _inet_internetreadfileex_function, wininet.internetreadfileex, wininet/InternetReadFileEx, wininet/InternetReadFileExA, wininet/InternetReadFileExW
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
req.unicode-ansi: InternetReadFileExW (Unicode) and InternetReadFileExA (ANSI)
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
 - InternetReadFileEx
 - InternetReadFileExA
 - InternetReadFileExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- InternetReadFileExA
: 
---

# InternetReadFileExA function


## -description


Reads data from a handle opened by the 
<a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a> or 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> function.


## -parameters




### -param hFile [in]

Handle returned by the 
<a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a> or 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> function.


### -param lpBuffersOut [out]

Pointer to an 
<a href="https://msdn.microsoft.com/9381184d-17f4-46ad-bd09-15c7e653d1b9">INTERNET_BUFFERS</a> structure that receives the data downloaded.


### -param dwFlags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_ASYNC</dt>
</dl>
</td>
<td width="60%">
Identical to  <a href="api_flags.htm">WININET_API_FLAG_ASYNC</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_SYNC</dt>
</dl>
</td>
<td width="60%">
Identical to <a href="api_flags.htm">WININET_API_FLAG_SYNC</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_USE_CONTEXT</dt>
</dl>
</td>
<td width="60%">
Identical to <a href="api_flags.htm">WININET_API_FLAG_USE_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_NO_WAIT</dt>
</dl>
</td>
<td width="60%">
Do not wait for data. If there is data available, the function returns either the amount of data requested or the amount of data available (whichever is smaller).

</td>
</tr>
</table>
 


### -param dwContext [in]

A caller supplied context value used for asynchronous operations.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. An application can also use 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a> when necessary.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

