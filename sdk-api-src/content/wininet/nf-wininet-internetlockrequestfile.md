---
UID: NF:wininet.InternetLockRequestFile
title: InternetLockRequestFile function (wininet.h)
author: windows-sdk-content
description: Places a lock on the file that is being used.
old-location: wininet\internetlockrequestfile.htm
tech.root: wininet
ms.assetid: 5924d117-1dcd-43d8-817e-02bda302bdd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InternetLockRequestFile, InternetLockRequestFile function [WinINet], _inet_internetlockrequestfile_function, wininet.internetlockrequestfile, wininet/InternetLockRequestFile
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - InternetLockRequestFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetLockRequestFile function


## -description


Places a lock on the file that is being used.


## -parameters




### -param hInternet [in]

Handle returned by 
the <a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a>, 
<a href="https://msdn.microsoft.com/2731d573-f981-48ce-a306-bb7e295cefc6">GopherOpenFile</a>, 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a>, or 
<a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a> function.


### -param lphLockRequestInfo [out]

Pointer to a handle that receives the lock request handle.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle passed to 
<i>hInternet</i> was created using 
<a href="https://msdn.microsoft.com/63027a3b-dc59-41c4-a22a-5d6e841159aa">INTERNET_FLAG_NO_CACHE_WRITE</a> or 
<a href="https://msdn.microsoft.com/63027a3b-dc59-41c4-a22a-5d6e841159aa">INTERNET_FLAG_DONT_CACHE</a>, the function creates a temporary file with the extension .tmp, unless it is an HTTPS resource. If the handle was created using <b>INTERNET_FLAG_NO_CACHE_WRITE</b> or <b>INTERNET_FLAG_DONT_CACHE</b> and it is accessing an HTTPS resource, 
<b>InternetLockRequestFile</b> fails.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/80747c0d-5a09-4ffa-a0ca-b051b82acbf8">Enabling Internet Functionality</a>



<a href="https://msdn.microsoft.com/356f7277-66ef-450f-ab5a-0303d0b1d807">InternetUnlockRequestFile</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

