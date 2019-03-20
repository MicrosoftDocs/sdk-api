---
UID: NF:wininet.InternetWriteFile
title: InternetWriteFile function (wininet.h)
author: windows-sdk-content
description: Writes data to an open Internet file.
old-location: wininet\internetwritefile.htm
tech.root: wininet
ms.assetid: 3bf8d4d8-9193-4aed-acf9-8d7207b332a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetWriteFile, InternetWriteFile function [WinINet], _inet_internetwritefile_function, wininet.internetwritefile, wininet/InternetWriteFile
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
 - InternetWriteFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetWriteFile function


## -description


Writes data to an open Internet file.


## -parameters




### -param hFile [in]

Handle returned from a previous call to 
<a href="https://msdn.microsoft.com/fb44d7bd-7868-4c53-aa4b-608d79c5bc7c">FtpOpenFile</a> or an 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle sent by 
<a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>.


### -param lpBuffer [in]

Pointer to a buffer that contains the data to be written to the file.


### -param dwNumberOfBytesToWrite [in]

Number of bytes to be written to the file.


### -param lpdwNumberOfBytesWritten [out]

Pointer to a variable that receives the number of bytes written to the file. 
<b>InternetWriteFile</b> sets this value to zero before doing any work or error checking.


## -returns



Returns TRUE if the function succeeds, or FALSE otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. An application can also use 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a> when necessary.




## -remarks



When the application is sending data, it must call 
<a href="https://msdn.microsoft.com/52b57e3c-3cfe-40bc-b87b-90cf39c5c38d">InternetCloseHandle</a> to end the data transfer.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

