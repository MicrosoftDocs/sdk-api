---
UID: NF:wininet.InternetQueryDataAvailable
title: InternetQueryDataAvailable function
author: windows-sdk-content
description: Queries the server to determine the amount of data available.
old-location: wininet\internetquerydataavailable.htm
tech.root: wininet
ms.assetid: fea8250d-f260-421f-b4dd-14b8685e8dac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetQueryDataAvailable, InternetQueryDataAvailable function [WinINet], _inet_internetquerydataavailable_function, wininet.internetquerydataavailable, wininet/InternetQueryDataAvailable
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
 - InternetQueryDataAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetQueryDataAvailable function


## -description


Queries the server to determine the amount of data available.


## -parameters




### -param hFile [in]

Handle returned by 
the <a href="https://msdn.microsoft.com/73f969c3-3fa7-43f5-88c5-ba78e59a8d1c">InternetOpenUrl</a>, 
<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a>, 
<a href="https://msdn.microsoft.com/2731d573-f981-48ce-a306-bb7e295cefc6">GopherOpenFile</a>, or 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> function.


### -param lpdwNumberOfBytesAvailable [out]

Pointer to a variable that receives the number of available bytes. May be <b>NULL</b>.


### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param dwContext [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns ERROR_NO_MORE_FILES.




## -remarks



This function returns the number of bytes of data that are available to be read immediately by a subsequent call to 
<a href="https://msdn.microsoft.com/1ec0fe70-4749-4251-9c58-44efdab74688">InternetReadFile</a>. If there is currently no data available and the end of the file has not been reached, the request waits until data becomes available. The amount of data remaining will not be recalculated until all available data indicated by the call to 
<b>InternetQueryDataAvailable</b> is read.

For 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handles created by 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> and sent by 
<a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>, a call to 
<a href="https://msdn.microsoft.com/6ea91da6-0bc2-49b6-a56b-c4224ad73b81">HttpEndRequest</a> must be made on the handle before 
<b>InternetQueryDataAvailable</b> can be used.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

