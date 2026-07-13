---
UID: NF:wininet.FtpFindFirstFileA
title: FtpFindFirstFileA function (wininet.h)
description: Searches the specified directory of the given FTP session. File and directory entries are returned to the application in the WIN32_FIND_DATA structure. (ANSI)
helpviewer_keywords: ["FtpFindFirstFileA", "wininet/FtpFindFirstFileA"]
old-location: wininet\ftpfindfirstfile.htm
tech.root: wininet
ms.assetid: 4f331f99-c52c-4744-a9a7-eeb09803862d
ms.date: 12/05/2018
ms.keywords: FtpFindFirstFile, FtpFindFirstFile function [WinINet], FtpFindFirstFileA, FtpFindFirstFileW, _inet_ftpfindfirstfile_function, wininet.ftpfindfirstfile, wininet/FtpFindFirstFile, wininet/FtpFindFirstFileA, wininet/FtpFindFirstFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpFindFirstFileW (Unicode) and FtpFindFirstFileA (ANSI)
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
 - FtpFindFirstFileA
 - wininet/FtpFindFirstFileA
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
 - FtpFindFirstFile
 - FtpFindFirstFileA
 - FtpFindFirstFileW
---

# FtpFindFirstFileA function


## -description

Searches the specified directory of the given FTP session. File and directory entries are returned to the application in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.

## -parameters

### -param hConnect [in]

Handle to an FTP session returned from 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>.

### -param lpszSearchFile [in]

Pointer to a <b>null</b>-terminated string that specifies a valid directory path or file name for the FTP server's file system. The string can contain wildcards, but no blank spaces are allowed. If the value of 
<i>lpszSearchFile</i> is <b>NULL</b> or if it is an empty string, the function  finds the first file in the current directory on the server.

### -param lpFindFileData [out]

Pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that receives information about the found file or directory.

### -param dwFlags [in]

Controls the behavior of this function. This parameter can be a combination of the following values.

<p class="indent">INTERNET_FLAG_HYPERLINK

<p class="indent">INTERNET_FLAG_NEED_FILE

<p class="indent">INTERNET_FLAG_NO_CACHE_WRITE

<p class="indent">INTERNET_FLAG_RELOAD

<p class="indent">INTERNET_FLAG_RESYNCHRONIZE

### -param dwContext [in]

Pointer to a variable that specifies the application-defined value that associates this search with any application data. This parameter is used only if the application has already called 
<a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a> to set up a status callback function.

## -returns

Returns a valid handle for the request if the directory enumeration was started successfully, or returns <b>NULL</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If <b>GetLastError</b> returns ERROR_INTERNET_EXTENDED_ERROR, as in the case where the function finds no matching files, call the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> function to retrieve the extended error text, as documented in <a href="/windows/desktop/WinInet/appendix-c-handling-errors">Handling Errors</a>.

## -remarks

For 
<b>FtpFindFirstFile</b>, file times returned in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure are in the local time zone, not in a coordinated universal time (UTC) format.

<b>FtpFindFirstFile</b> is similar to the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> function. Note, however, that only one 
<b>FtpFindFirstFile</b> can occur at a time within a given FTP session. The enumerations, therefore, are correlated with the FTP session handle. This is because the FTP protocol allows only a single directory enumeration per session.

After calling 
<b>FtpFindFirstFile</b> and until calling 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a>, the application cannot call 
<b>FtpFindFirstFile</b> again on the given FTP session handle. If a call is made to 
<b>FtpFindFirstFile</b> on that handle, the function  fails with 
<a href="/windows/desktop/WinInet/wininet-errors">ERROR_FTP_TRANSFER_IN_PROGRESS</a>. After the calling application has finished using the 
<b>HINTERNET</b> handle returned by 
<b>FtpFindFirstFile</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.

After beginning a directory enumeration with 
<b>FtpFindFirstFile</b>, the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a> function can be used to continue the enumeration.

Because the FTP protocol provides no standard means of enumerating, some of the common information about files, such as file creation date and time, is not always available or correct. When this happens, 
<b>FtpFindFirstFile</b> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetfindnextfilea">InternetFindNextFile</a> fill in unavailable information with a best guess based on available information. For example, creation and last access dates are often  the same as the file's modification date.

The application cannot call 
<b>FtpFindFirstFile</b> between calls to 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpFindFirstFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
