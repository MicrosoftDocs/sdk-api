---
UID: NF:wininet.FtpDeleteFileW
title: FtpDeleteFileW function (wininet.h)
description: Deletes a file stored on the FTP server. (Unicode)
helpviewer_keywords: ["FtpDeleteFile", "FtpDeleteFile function [WinINet]", "FtpDeleteFileW", "_inet_ftpdeletefile_function", "wininet.ftpdeletefile", "wininet/FtpDeleteFile", "wininet/FtpDeleteFileW"]
old-location: wininet\ftpdeletefile.htm
tech.root: wininet
ms.assetid: 16723c97-fd6f-40c2-844d-fc6d2dcc1a32
ms.date: 12/05/2018
ms.keywords: FtpDeleteFile, FtpDeleteFile function [WinINet], FtpDeleteFileA, FtpDeleteFileW, _inet_ftpdeletefile_function, wininet.ftpdeletefile, wininet/FtpDeleteFile, wininet/FtpDeleteFileA, wininet/FtpDeleteFileW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FtpDeleteFileW
 - wininet/FtpDeleteFileW
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
 - FtpDeleteFile
 - FtpDeleteFileA
 - FtpDeleteFileW
---

# FtpDeleteFileW function


## -description

Deletes a file stored on the FTP server.

## -parameters

### -param hConnect [in]

Handle returned by a previous call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a> using <b>INTERNET_SERVICE_FTP</b>.

### -param lpszFileName [in]

Pointer to a null-terminated string that contains the name of the file to be deleted.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<i>lpszFileName</i> parameter can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpDeleteFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
