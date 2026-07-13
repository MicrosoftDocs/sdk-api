---
UID: NF:wininet.FtpOpenFileW
title: FtpOpenFileW function (wininet.h)
description: Initiates access to a remote file on an FTP server for reading or writing. (Unicode)
helpviewer_keywords: ["FTP_TRANSFER_TYPE_ASCII", "FTP_TRANSFER_TYPE_BINARY", "FTP_TRANSFER_TYPE_UNKNOWN", "FtpOpenFile", "FtpOpenFile function [WinINet]", "FtpOpenFileW", "INTERNET_FLAG_HYPERLINK", "INTERNET_FLAG_NEED_FILE", "INTERNET_FLAG_RELOAD", "INTERNET_FLAG_RESYNCHRONIZE", "INTERNET_FLAG_TRANSFER_ASCII", "INTERNET_FLAG_TRANSFER_BINARY", "_inet_ftpopenfile_function", "wininet.ftpopenfile", "wininet/FtpOpenFile", "wininet/FtpOpenFileW"]
old-location: wininet\ftpopenfile.htm
tech.root: wininet
ms.assetid: fb44d7bd-7868-4c53-aa4b-608d79c5bc7c
ms.date: 12/05/2018
ms.keywords: FTP_TRANSFER_TYPE_ASCII, FTP_TRANSFER_TYPE_BINARY, FTP_TRANSFER_TYPE_UNKNOWN, FtpOpenFile, FtpOpenFile function [WinINet], FtpOpenFileA, FtpOpenFileW, INTERNET_FLAG_HYPERLINK, INTERNET_FLAG_NEED_FILE, INTERNET_FLAG_RELOAD, INTERNET_FLAG_RESYNCHRONIZE, INTERNET_FLAG_TRANSFER_ASCII, INTERNET_FLAG_TRANSFER_BINARY, _inet_ftpopenfile_function, wininet.ftpopenfile, wininet/FtpOpenFile, wininet/FtpOpenFileA, wininet/FtpOpenFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpOpenFileW (Unicode) and FtpOpenFileA (ANSI)
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
 - FtpOpenFileW
 - wininet/FtpOpenFileW
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
 - FtpOpenFile
 - FtpOpenFileA
 - FtpOpenFileW
---

# FtpOpenFileW function


## -description

Initiates access to a remote file on an FTP server for reading or writing.

## -parameters

### -param hConnect [in]

Handle to an FTP session.

### -param lpszFileName [in]

Pointer to a null-terminated string that contains the name of the file to be accessed.

### -param dwAccess [in]

File  access. This parameter can be <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b>, but not both.

### -param dwFlags [in]

Conditions under which the transfers occur. The application should select one transfer type and any of the flags that indicate how the caching of the file will be controlled.


The transfer type can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FTP_TRANSFER_TYPE_ASCII"></a><a id="ftp_transfer_type_ascii"></a><dl>
<dt><b>FTP_TRANSFER_TYPE_ASCII</b></dt>
</dl>
</td>
<td width="60%">
Transfers the file using FTP's ASCII (Type A) transfer method. Control and formatting information is converted to local equivalents.

</td>
</tr>
<tr>
<td width="40%"><a id="FTP_TRANSFER_TYPE_BINARY"></a><a id="ftp_transfer_type_binary"></a><dl>
<dt><b>FTP_TRANSFER_TYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Transfers the file using FTP's Image (Type I) transfer method. The file is transferred exactly as it exists with no changes. This is the default transfer method.

</td>
</tr>
<tr>
<td width="40%"><a id="FTP_TRANSFER_TYPE_UNKNOWN"></a><a id="ftp_transfer_type_unknown"></a><dl>
<dt><b>FTP_TRANSFER_TYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Defaults to FTP_TRANSFER_TYPE_BINARY.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_TRANSFER_ASCII"></a><a id="internet_flag_transfer_ascii"></a><dl>
<dt><b>INTERNET_FLAG_TRANSFER_ASCII</b></dt>
</dl>
</td>
<td width="60%">
Transfers the file as ASCII.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_TRANSFER_BINARY"></a><a id="internet_flag_transfer_binary"></a><dl>
<dt><b>INTERNET_FLAG_TRANSFER_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Transfers the file as binary.

</td>
</tr>
</table>
 


The following values are used to control the caching of the file. The application can use one or more of these values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_HYPERLINK"></a><a id="internet_flag_hyperlink"></a><dl>
<dt><b>INTERNET_FLAG_HYPERLINK</b></dt>
</dl>
</td>
<td width="60%">
Forces a reload if there was no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_NEED_FILE"></a><a id="internet_flag_need_file"></a><dl>
<dt><b>INTERNET_FLAG_NEED_FILE</b></dt>
</dl>
</td>
<td width="60%">
Causes a temporary file to be created if the file cannot be cached.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_RELOAD"></a><a id="internet_flag_reload"></a><dl>
<dt><b>INTERNET_FLAG_RELOAD</b></dt>
</dl>
</td>
<td width="60%">
Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_RESYNCHRONIZE"></a><a id="internet_flag_resynchronize"></a><dl>
<dt><b>INTERNET_FLAG_RESYNCHRONIZE</b></dt>
</dl>
</td>
<td width="60%">
Reloads HTTP resources if the resource has been modified since the last time it was downloaded. All FTP resources are reloaded.

<b>Windows XP and Windows Server 2003 R2 and earlier:  </b>Gopher resources are also reloaded.

</td>
</tr>
</table>

### -param dwContext [in]

Pointer to a variable that contains the application-defined value that associates this search with any application data. This is only used if the application has already called 
<a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a> to set up a status callback function.

## -returns

Returns a handle if successful, or <b>NULL</b> otherwise. To retrieve a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After calling 
<b>FtpOpenFile</b> and until calling 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a>, all other calls to FTP functions on the same FTP session handle will fail and set the error message to 
<a href="/windows/desktop/WinInet/wininet-errors">ERROR_FTP_TRANSFER_IN_PROGRESS</a>. After the calling application has finished using the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle returned by 
<b>FtpOpenFile</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.

Only one file can be open in a single FTP session. Therefore, no file handle is returned and the application simply uses the FTP session handle when necessary.

Error 12058 can occur if **FtpOpenFileW** fails due to a lack of available local ports.

The 
<i>lpszFileName</i> parameter can be either a partially or fully qualified file name relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpOpenFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
