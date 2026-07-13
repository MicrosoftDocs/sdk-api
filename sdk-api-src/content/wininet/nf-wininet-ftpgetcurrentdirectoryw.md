---
UID: NF:wininet.FtpGetCurrentDirectoryW
title: FtpGetCurrentDirectoryW function (wininet.h)
description: Retrieves the current directory for the specified FTP session. (Unicode)
helpviewer_keywords: ["FtpGetCurrentDirectory", "FtpGetCurrentDirectory function [WinINet]", "FtpGetCurrentDirectoryW", "_inet_ftpgetcurrentdirectory_function", "wininet.ftpgetcurrentdirectory", "wininet/FtpGetCurrentDirectory", "wininet/FtpGetCurrentDirectoryW"]
old-location: wininet\ftpgetcurrentdirectory.htm
tech.root: wininet
ms.assetid: 1b757061-469b-4c11-9d0d-38b300216221
ms.date: 12/05/2018
ms.keywords: FtpGetCurrentDirectory, FtpGetCurrentDirectory function [WinINet], FtpGetCurrentDirectoryA, FtpGetCurrentDirectoryW, _inet_ftpgetcurrentdirectory_function, wininet.ftpgetcurrentdirectory, wininet/FtpGetCurrentDirectory, wininet/FtpGetCurrentDirectoryA, wininet/FtpGetCurrentDirectoryW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpGetCurrentDirectoryW (Unicode) and FtpGetCurrentDirectoryA (ANSI)
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
 - FtpGetCurrentDirectoryW
 - wininet/FtpGetCurrentDirectoryW
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
 - FtpGetCurrentDirectory
 - FtpGetCurrentDirectoryA
 - FtpGetCurrentDirectoryW
---

# FtpGetCurrentDirectoryW function


## -description

Retrieves the current directory for the specified FTP session.

## -parameters

### -param hConnect [in]

Handle to an FTP session.

### -param lpszCurrentDirectory [out]

Pointer to a null-terminated string that receives the absolute path of the current directory.

### -param lpdwCurrentDirectory [in, out]

Pointer to a variable that specifies the length of the buffer, in <b>TCHARs</b>. The buffer length must include room for a terminating null character. Using a length of <b>MAX_PATH</b> is sufficient for all paths. When the function returns, the variable receives the number of characters copied into the buffer.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the 
<i>lpszCurrentDirectory</i> buffer is not large enough, 
<i>lpdwCurrentDirectory</i> receives the number of bytes required to retrieve the full, current directory name.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpGetCurrentDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-ftpsetcurrentdirectorya">FtpSetCurrentDirectory</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
