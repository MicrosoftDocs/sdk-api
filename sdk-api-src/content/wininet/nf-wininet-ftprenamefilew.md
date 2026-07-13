---
UID: NF:wininet.FtpRenameFileW
title: FtpRenameFileW function (wininet.h)
description: Renames a file stored on the FTP server. (Unicode)
helpviewer_keywords: ["FtpRenameFile", "FtpRenameFile function [WinINet]", "FtpRenameFileW", "_inet_ftprenamefile_function", "wininet.ftprenamefile", "wininet/FtpRenameFile", "wininet/FtpRenameFileW"]
old-location: wininet\ftprenamefile.htm
tech.root: wininet
ms.assetid: 2c46d8bb-aceb-4dd2-be4f-2c418357d4ae
ms.date: 12/05/2018
ms.keywords: FtpRenameFile, FtpRenameFile function [WinINet], FtpRenameFileA, FtpRenameFileW, _inet_ftprenamefile_function, wininet.ftprenamefile, wininet/FtpRenameFile, wininet/FtpRenameFileA, wininet/FtpRenameFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpRenameFileW (Unicode) and FtpRenameFileA (ANSI)
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
 - FtpRenameFileW
 - wininet/FtpRenameFileW
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
 - FtpRenameFile
 - FtpRenameFileA
 - FtpRenameFileW
---

# FtpRenameFileW function


## -description

Renames a file stored on the FTP server.

## -parameters

### -param hConnect [in]

Handle to an FTP session.

### -param lpszExisting [in]

Pointer to a null-terminated string that contains the name of the file to be renamed.

### -param lpszNew [in]

Pointer to a null-terminated string that contains the new name for the remote file.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<i>lpszExisting</i> and 
<i>lpszNew</i> parameters can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpRenameFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
