---
UID: NF:wininet.FtpRemoveDirectoryW
title: FtpRemoveDirectoryW function (wininet.h)
description: Removes the specified directory on the FTP server.helpviewer_keywords: ["FtpRemoveDirectory","FtpRemoveDirectory function [WinINet]","FtpRemoveDirectoryA","FtpRemoveDirectoryW","_inet_ftpremovedirectory_function","wininet.ftpremovedirectory","wininet/FtpRemoveDirectory","wininet/FtpRemoveDirectoryA","wininet/FtpRemoveDirectoryW"]
old-location: wininet\ftpremovedirectory.htm
tech.root: wininet
ms.assetid: 4c02af2f-ece8-409a-9c3e-495e1beb80ef
ms.date: 12/05/2018
ms.keywords: FtpRemoveDirectory, FtpRemoveDirectory function [WinINet], FtpRemoveDirectoryA, FtpRemoveDirectoryW, _inet_ftpremovedirectory_function, wininet.ftpremovedirectory, wininet/FtpRemoveDirectory, wininet/FtpRemoveDirectoryA, wininet/FtpRemoveDirectoryW
f1_keywords:
- wininet/FtpRemoveDirectory
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
req.unicode-ansi: FtpRemoveDirectoryW (Unicode) and FtpRemoveDirectoryA (ANSI)
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
- FtpRemoveDirectory
- FtpRemoveDirectoryA
- FtpRemoveDirectoryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FtpRemoveDirectoryW function


## -description


Removes the specified directory on the FTP server.


## -parameters




### -param hConnect [in]

Handle to an FTP session.


### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to be removed. This can be either a fully qualified path or a name relative to the current directory.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the error message indicates that the FTP server denied the request to remove a directory, use 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> to determine why.




## -remarks



An application should use 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-ftpgetcurrentdirectorya">FtpGetCurrentDirectory</a> to determine the remote site's current working directory, instead of assuming that the remote system uses a hierarchical naming scheme for directories.

The 
<i>lpszDirectory</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
 

 

