---
UID: NF:wininet.FtpRemoveDirectoryA
title: FtpRemoveDirectoryA function (wininet.h)
description: Removes the specified directory on the FTP server. (ANSI)
helpviewer_keywords: ["FtpRemoveDirectoryA", "wininet/FtpRemoveDirectoryA"]
old-location: wininet\ftpremovedirectory.htm
tech.root: wininet
ms.assetid: 4c02af2f-ece8-409a-9c3e-495e1beb80ef
ms.date: 12/05/2018
ms.keywords: FtpRemoveDirectory, FtpRemoveDirectory function [WinINet], FtpRemoveDirectoryA, FtpRemoveDirectoryW, _inet_ftpremovedirectory_function, wininet.ftpremovedirectory, wininet/FtpRemoveDirectory, wininet/FtpRemoveDirectoryA, wininet/FtpRemoveDirectoryW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FtpRemoveDirectoryA
 - wininet/FtpRemoveDirectoryA
dev_langs:
 - c++
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
---

# FtpRemoveDirectoryA function


## -description

Removes the specified directory on the FTP server.

## -parameters

### -param hConnect [in]

Handle to an FTP session.

### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to be removed. This can be either a fully qualified path or a name relative to the current directory.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the error message indicates that the FTP server denied the request to remove a directory, use 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> to determine why.

## -remarks

An application should use 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpgetcurrentdirectorya">FtpGetCurrentDirectory</a> to determine the remote site's current working directory, instead of assuming that the remote system uses a hierarchical naming scheme for directories.

The 
<i>lpszDirectory</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpRemoveDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
