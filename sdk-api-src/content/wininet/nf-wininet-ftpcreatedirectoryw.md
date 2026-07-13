---
UID: NF:wininet.FtpCreateDirectoryW
title: FtpCreateDirectoryW function (wininet.h)
description: Creates a new directory on the FTP server. (Unicode)
helpviewer_keywords: ["FtpCreateDirectory", "FtpCreateDirectory function [WinINet]", "FtpCreateDirectoryW", "_inet_ftpcreatedirectory_function", "wininet.ftpcreatedirectory", "wininet/FtpCreateDirectory", "wininet/FtpCreateDirectoryW"]
old-location: wininet\ftpcreatedirectory.htm
tech.root: wininet
ms.assetid: 51a33c5b-4e82-4148-8a3f-0cf7c0a8bac0
ms.date: 12/05/2018
ms.keywords: FtpCreateDirectory, FtpCreateDirectory function [WinINet], FtpCreateDirectoryA, FtpCreateDirectoryW, _inet_ftpcreatedirectory_function, wininet.ftpcreatedirectory, wininet/FtpCreateDirectory, wininet/FtpCreateDirectoryA, wininet/FtpCreateDirectoryW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpCreateDirectoryW (Unicode) and FtpCreateDirectoryA (ANSI)
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
 - FtpCreateDirectoryW
 - wininet/FtpCreateDirectoryW
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
 - FtpCreateDirectory
 - FtpCreateDirectoryA
 - FtpCreateDirectoryW
---

# FtpCreateDirectoryW function


## -description

Creates a new directory on the FTP server.

## -parameters

### -param hConnect [in]

Handle returned by a previous call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a> using <b>INTERNET_SERVICE_FTP</b>.

### -param lpszDirectory [in]

Pointer to a null-terminated string that contains the name of the directory to be created. This can be either a fully qualified path or a name relative to the current directory.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the error message indicates that the FTP server denied the request to create a directory, use 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> to determine why.

## -remarks

An application should use 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpgetcurrentdirectorya">FtpGetCurrentDirectory</a> to determine the remote site's current working directory instead of assuming that the remote system uses a hierarchical naming scheme for directories.

The 
<i>lpszDirectory</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpCreateDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
