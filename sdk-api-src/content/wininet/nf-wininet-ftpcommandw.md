---
UID: NF:wininet.FtpCommandW
title: FtpCommandW function (wininet.h)
description: Sends commands directly to an FTP server. (Unicode)
helpviewer_keywords: ["FTP_TRANSFER_TYPE_ASCII", "FTP_TRANSFER_TYPE_BINARY", "FtpCommand", "FtpCommand function [WinINet]", "FtpCommandW", "_inet_ftpcommand_function", "wininet.ftpcommand", "wininet/FtpCommand", "wininet/FtpCommandW"]
old-location: wininet\ftpcommand.htm
tech.root: wininet
ms.assetid: cd12f52c-80d6-4aee-96c8-cb3cafcf0a6a
ms.date: 12/05/2018
ms.keywords: FTP_TRANSFER_TYPE_ASCII, FTP_TRANSFER_TYPE_BINARY, FtpCommand, FtpCommand function [WinINet], FtpCommandA, FtpCommandW, _inet_ftpcommand_function, wininet.ftpcommand, wininet/FtpCommand, wininet/FtpCommandA, wininet/FtpCommandW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FtpCommandW (Unicode) and FtpCommandA (ANSI)
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
 - FtpCommandW
 - wininet/FtpCommandW
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
 - FtpCommand
 - FtpCommandA
 - FtpCommandW
---

# FtpCommandW function


## -description

The <b>FtpCommand</b> function sends commands directly to an FTP server.

## -parameters

### -param hConnect [in]

A handle returned from a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a>.

### -param fExpectResponse [in]

A Boolean value that indicates whether the application expects a data connection to be established by the FTP server. This must be set to <b>TRUE</b> if a data connection is expected, or <b>FALSE</b> otherwise.

### -param dwFlags [in]

A parameter that can be set to one of the following values.

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
Transfers the file using the FTP ASCII (Type A) transfer method. Control and formatting data is converted to local equivalents.

</td>
</tr>
<tr>
<td width="40%"><a id="FTP_TRANSFER_TYPE_BINARY"></a><a id="ftp_transfer_type_binary"></a><dl>
<dt><b>FTP_TRANSFER_TYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Transfers the file using the FTP Image (Type I) transfer method. The file is transferred exactly with no changes. This is the default transfer method.

</td>
</tr>
</table>

### -param lpszCommand [in]

A pointer to a string that contains the command to send to the FTP server.

### -param dwContext [in]

A pointer to a variable that contains an application-defined value used to identify the application context in callback operations.

### -param phFtpCommand [out]

A pointer to a handle that is created if a valid data socket is opened. The 
<i>fExpectResponse</i> parameter must be set to <b>TRUE</b> for 
<i>phFtpCommand</i> to be filled.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can return 
<a href="/windows/desktop/WinInet/wininet-errors">ERROR_INTERNET_NO_DIRECT_ACCESS</a> if the client application is offline. If one or more of the parameters are invalid, 
<b>GetLastError</b> will return <b>ERROR_INVALID_PARAMETER</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FtpCommand as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/ftp-sessions">FTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
