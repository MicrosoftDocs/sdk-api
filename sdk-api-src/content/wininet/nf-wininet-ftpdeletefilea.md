---
UID: NF:wininet.FtpDeleteFileA
title: FtpDeleteFileA function (wininet.h)
description: Deletes a file stored on the FTP server.helpviewer_keywords: ["FtpDeleteFile","FtpDeleteFile function [WinINet]","FtpDeleteFileA","FtpDeleteFileW","_inet_ftpdeletefile_function","wininet.ftpdeletefile","wininet/FtpDeleteFile","wininet/FtpDeleteFileA","wininet/FtpDeleteFileW"]
old-location: wininet\ftpdeletefile.htm
tech.root: wininet
ms.assetid: 16723c97-fd6f-40c2-844d-fc6d2dcc1a32
ms.date: 12/05/2018
ms.keywords: FtpDeleteFile, FtpDeleteFile function [WinINet], FtpDeleteFileA, FtpDeleteFileW, _inet_ftpdeletefile_function, wininet.ftpdeletefile, wininet/FtpDeleteFile, wininet/FtpDeleteFileA, wininet/FtpDeleteFileW
f1_keywords:
- wininet/FtpDeleteFile
dev_langs:
- c++
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpDeleteFileW (Unicode) and FtpDeleteFileA (ANSI)
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
- FtpDeleteFile
- FtpDeleteFileA
- FtpDeleteFileW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FtpDeleteFileA function


## -description


Deletes a file stored on the FTP server.


## -parameters




### -param hConnect [in]

Handle returned by a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a> using <b>INTERNET_SERVICE_FTP</b>.


### -param lpszFileName [in]

Pointer to a null-terminated string that contains the name of the file to be deleted.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<i>lpszFileName</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

