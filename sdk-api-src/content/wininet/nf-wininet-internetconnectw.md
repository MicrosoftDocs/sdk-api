---
UID: NF:wininet.InternetConnectW
title: InternetConnectW function (wininet.h)
description: Opens an File Transfer Protocol (FTP) or HTTP session for a given site. (Unicode)
helpviewer_keywords: ["InternetConnect", "InternetConnect function [WinINet]", "InternetConnectW", "_win32_internetconnect", "wininet.internetconnect", "wininet/InternetConnect", "wininet/InternetConnectW"]
old-location: wininet\internetconnect.htm
tech.root: wininet
ms.assetid: 42b5d733-dccd-4c9d-8820-e358e033077c
ms.date: 12/05/2018
ms.keywords: InternetConnect, InternetConnect function [WinINet], InternetConnectA, InternetConnectW, _win32_internetconnect, wininet.internetconnect, wininet/InternetConnect, wininet/InternetConnectA, wininet/InternetConnectW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetConnectW (Unicode) and InternetConnectA (ANSI)
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
 - InternetConnectW
 - wininet/InternetConnectW
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
 - InternetConnect
 - InternetConnectA
 - InternetConnectW
---

# InternetConnectW function


## -description

Opens an File Transfer Protocol (FTP) or HTTP session for a given site.

## -parameters

### -param hInternet [in]

Handle returned by a previous call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a>.

### -param lpszServerName [in]

Pointer to a <b>null</b>-terminated string that specifies the host name of an Internet server. Alternately, the string can contain the IP number of the site, in ASCII dotted-decimal format (for example, 11.0.1.45).

### -param nServerPort [in]

Transmission Control Protocol/Internet Protocol (TCP/IP) port on the server. These flags set only the port that is used. The service is set by the value of 
<i>dwService</i>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DEFAULT_FTP_PORT</dt>
</dl>
</td>
<td width="60%">
Uses the default port for FTP servers (port 21).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DEFAULT_GOPHER_PORT</dt>
</dl>
</td>
<td width="60%">
Uses the default port for Gopher servers (port 70).<div class="alert"><b>Note</b>  Windows XP and Windows Server 2003 R2 and earlier only.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DEFAULT_HTTP_PORT</dt>
</dl>
</td>
<td width="60%">
Uses the default port for HTTP servers (port 80).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DEFAULT_HTTPS_PORT</dt>
</dl>
</td>
<td width="60%">
Uses the default port for Secure Hypertext Transfer Protocol (HTTPS) servers (port 443).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DEFAULT_SOCKS_PORT</dt>
</dl>
</td>
<td width="60%">
Uses the default port for SOCKS firewall servers (port 1080).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_INVALID_PORT_NUMBER</dt>
</dl>
</td>
<td width="60%">
Uses the default port for the service specified by 
<i>dwService</i>.

</td>
</tr>
</table>

### -param lpszUserName [in]

Pointer to a <b>null</b>-terminated string that specifies the name of the user to log on. If this parameter is <b>NULL</b>, the function uses an appropriate default. For the FTP protocol, the default is "anonymous".

### -param lpszPassword [in]

Pointer to a <b>null</b>-terminated string that contains the password to use to log on. If both 
<i>lpszPassword</i> and 
<i>lpszUsername</i> are <b>NULL</b>, the function uses the default "anonymous" password. In the case of FTP, the default password is the user's email name. If 
<i>lpszPassword</i> is <b>NULL</b>, but 
<i>lpszUsername</i> is not <b>NULL</b>, the function uses a blank password.

### -param dwService [in]

Type of service to access. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_SERVICE_FTP</dt>
</dl>
</td>
<td width="60%">
FTP service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_SERVICE_GOPHER</dt>
</dl>
</td>
<td width="60%">
Gopher service.<div class="alert"><b>Note</b>  Windows XP and Windows Server 2003 R2 and earlier only.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_SERVICE_HTTP</dt>
</dl>
</td>
<td width="60%">
HTTP service.

</td>
</tr>
</table>

### -param dwFlags [in]

Options specific to the service used. If  
<i>dwService</i> is INTERNET_SERVICE_FTP, 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_PASSIVE</a> causes the application to use passive FTP semantics.

### -param dwContext [in]

Pointer to a variable that contains an application-defined value that is used to identify the application context for the returned handle in callbacks.

## -returns

Returns a valid handle to the session if the connection is successful, or <b>NULL</b> otherwise. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. An application can also use 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> to determine why access to the service was denied.

## -remarks

The following table describes the behavior for the four possible settings of 
<i>lpszUsername</i> and 
<i>lpszPassword</i>. 
				
<table class="clsStd">
<tr>
<th><i>lpszUsername</i></th>
<th><i>lpszPassword</i></th>
<th>User name sent to FTP server</th>
<th>Password sent to FTP server</th>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
<td>"anonymous"</td>
<td>User's email name</td>
</tr>
<tr>
<td>Non-<b>NULL</b> string</td>
<td><b>NULL</b></td>
<td><i>lpszUsername</i></td>
<td>""</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>Non-<b>NULL</b> string</td>
<td>ERROR</td>
<td>ERROR</td>
</tr>
<tr>
<td>Non-<b>NULL</b> string</td>
<td>Non-<b>NULL</b> string</td>
<td><i>lpszUsername</i></td>
<td><i>lpszPassword</i></td>
</tr>
</table>
 



For FTP sites, 
<b>InternetConnect</b> actually establishes a connection with the server; for others, the actual connection is not established until the application requests a specific transaction.

For maximum efficiency, applications using the HTTP protocols should try to minimize calls to 
<b>InternetConnect</b> and avoid calling this function for every transaction requested by the user. One way to accomplish this is to keep a small cache of handles returned from 
<b>InternetConnect</b>; when the user makes a request to a previously accessed server, that session handle is still available.

After the calling application has finished using the 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle returned by 
<b>InternetConnect</b>, it must be closed using the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> function.


<b>Note</b>  When a request is sent asynchronous mode (the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a> specifies <b>INTERNET_FLAG_ASYNC</b>), and the <i>dwContext</i> parameter is zero (<b>INTERNET_NO_CALLBACK</b>), the callback function set with <a href="/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback">InternetSetStatusCallback</a> on the connection handle will not be called, however, the call will still be performed in asynchronous mode.  




Examples of <b>InternetConnect</b> usage can be found in the following topics.

<ul>
<li>
<a href="/windows/desktop/WinInet/handling-authentication">Handling Authentication</a>
</li>
<li>
<a href="/windows/desktop/WinInet/asynchronous-example-application">Asynchronous Example Application</a>
</li>
</ul>


Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetConnect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
