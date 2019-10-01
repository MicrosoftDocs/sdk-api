---
UID: NF:wininet.InternetWriteFile
title: InternetWriteFile function (wininet.h)
author: windows-sdk-content
description: Writes data to an open Internet file.
old-location: wininet\internetwritefile.htm
tech.root: wininet
ms.assetid: 3bf8d4d8-9193-4aed-acf9-8d7207b332a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InternetWriteFile, InternetWriteFile function [WinINet], _inet_internetwritefile_function, wininet.internetwritefile, wininet/InternetWriteFile
ms.topic: function
f1_keywords: 
 - "wininet/InternetWriteFile"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetWriteFile function


## -description


Writes data to an open Internet file.


## -parameters




### -param hFile [in]

Handle returned from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a> or an 
<a href="https://docs.microsoft.com/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle sent by 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa">HttpSendRequestEx</a>.


### -param lpBuffer [in]

Pointer to a buffer that contains the data to be written to the file.


### -param dwNumberOfBytesToWrite [in]

Number of bytes to be written to the file.


### -param lpdwNumberOfBytesWritten [out]

Pointer to a variable that receives the number of bytes written to the file. 
<b>InternetWriteFile</b> sets this value to zero before doing any work or error checking.


## -returns



Returns TRUE if the function succeeds, or FALSE otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. An application can also use 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> when necessary.




## -remarks



When the application is sending data, it must call 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> to end the data transfer.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

