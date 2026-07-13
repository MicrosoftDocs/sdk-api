---
UID: NF:wininet.FtpGetFileA
title: FtpGetFileA function (wininet.h)
description: Retrieves a file from the FTP server and stores it under the specified file name, creating a new local file in the process. (ANSI)
helpviewer_keywords: ["FTP_TRANSFER_TYPE_ASCII", "FTP_TRANSFER_TYPE_BINARY", "FTP_TRANSFER_TYPE_UNKNOWN", "FtpGetFileA", "INTERNET_FLAG_HYPERLINK", "INTERNET_FLAG_NEED_FILE", "INTERNET_FLAG_RELOAD", "INTERNET_FLAG_RESYNCHRONIZE", "INTERNET_FLAG_TRANSFER_ASCII", "INTERNET_FLAG_TRANSFER_BINARY", "wininet/FtpGetFileA"]
old-location: wininet\ftpgetfile.htm
tech.root: wininet
ms.assetid: 2de83924-dc48-42bc-8f08-b94e9eb88b6f
ms.date: 12/05/2018
ms.keywords: FTP_TRANSFER_TYPE_ASCII, FTP_TRANSFER_TYPE_BINARY, FTP_TRANSFER_TYPE_UNKNOWN, FtpGetFile, FtpGetFile function [WinINet], FtpGetFileA, FtpGetFileW, INTERNET_FLAG_HYPERLINK, INTERNET_FLAG_NEED_FILE, INTERNET_FLAG_RELOAD, INTERNET_FLAG_RESYNCHRONIZE, INTERNET_FLAG_TRANSFER_ASCII, INTERNET_FLAG_TRANSFER_BINARY, _win32_ftpgetfile, wininet.ftpgetfile, wininet/FtpGetFile, wininet/FtpGetFileA, wininet/FtpGetFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpGetFileW (Unicode) and FtpGetFileA (ANSI)
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
 - FtpGetFileA
 - wininet/FtpGetFileA
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
 - FtpGetFile
 - FtpGetFileA
 - FtpGetFileW
---

# FtpGetFileA function


## -description

Retrieves a file from the FTP server and stores it under the specified file name, creating a new local file in the process.

## -parameters

### -param hConnect [in]

Handle to an FTP session.

### -param lpszRemoteFile [in]

Pointer to a null-terminated string that contains the name of the file to be retrieved.

### -param lpszNewFile [in]

Pointer to a null-terminated string that contains the name of the file to be created on the local system.

### -param fFailIfExists [in]

Indicates whether the function should proceed if a local file of the specified name already exists. If 
<i>fFailIfExists</i> is <b>TRUE</b> and the local file exists, 
<b>FtpGetFile</b> fails.

### -param dwFlagsAndAttributes [in]

File attributes for the new file. This parameter can be any combination of the FILE_ATTRIBUTE_* flags used by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwFlags [in]

Controls how the function will handle the file download. The first set of flag values indicates the conditions under which the transfer occurs. These transfer type flags can be used in combination with the second set of flags that control caching.


The application can select one of these transfer type values.



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
 


The following flags determine how the caching of this file will be done. Any combination of the following flags can be used with the transfer type flag.



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

Pointer to a variable that contains the application-defined value that associates this search with any application data. This is used only if the application has already called 
<a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a> to set up a status callback function.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>FtpGetFile</b> is a high-level routine that handles all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally. An application that needs to retrieve file data only or that requires close control over the file transfer should use the 
<a href="/windows/desktop/api/wininet/nf-wininet-ftpopenfilea">FtpOpenFile</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-internetreadfile">InternetReadFile</a> functions.

If the 
<i>dwFlags</i> parameter specifies <b>FTP_TRANSFER_TYPE_ASCII</b>, translation of the file data converts control and formatting characters to local equivalents. The default transfer is binary mode, where the file is downloaded in the same format as it is stored on the server.

Both 
<i>lpszRemoteFile</i> and 
<i>lpszNewFile</i> can be either partially or fully qualified file names relative to the current directory.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpGetFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
