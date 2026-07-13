---
UID: NF:wininet.InternetCheckConnectionW
title: InternetCheckConnectionW function (wininet.h)
description: Allows an application to check if a connection to the Internet can be established. (Unicode)
helpviewer_keywords: ["InternetCheckConnection", "InternetCheckConnection function [WinINet]", "InternetCheckConnectionW", "_inet_internetcheckconnection_function", "wininet.internetcheckconnection", "wininet/InternetCheckConnection", "wininet/InternetCheckConnectionW"]
old-location: wininet\internetcheckconnection.htm
tech.root: wininet
ms.assetid: 4666e4ee-057e-452d-ac2c-d03321a0073f
ms.date: 12/05/2018
ms.keywords: InternetCheckConnection, InternetCheckConnection function [WinINet], InternetCheckConnectionA, InternetCheckConnectionW, _inet_internetcheckconnection_function, wininet.internetcheckconnection, wininet/InternetCheckConnection, wininet/InternetCheckConnectionA, wininet/InternetCheckConnectionW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetCheckConnectionW (Unicode) and InternetCheckConnectionA (ANSI)
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
 - InternetCheckConnectionW
 - wininet/InternetCheckConnectionW
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
 - InternetCheckConnection
 - InternetCheckConnectionA
 - InternetCheckConnectionW
---

# InternetCheckConnectionW function


## -description

<p class="CCE_Message">[<b>InternetCheckConnection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/uwp/api/Windows.Networking.Connectivity.NetworkInformation#Windows_Networking_Connectivity_NetworkInformation_GetInternetConnectionProfile_">NetworkInformation.GetInternetConnectionProfile</a> or the <a href="/windows/desktop/NLA/nlm-interfaces">NLM Interfaces</a>.
]

Allows an application to check if a connection to the Internet can be established.

## -parameters

### -param lpszUrl [in]

Pointer to a <b>null</b>-terminated string that specifies the URL to use to check the connection. This value can be <b>NULL</b>.

### -param dwFlags [in]

Options. FLAG_ICC_FORCE_CONNECTION is the only flag that is currently available. If this flag is set, it forces a connection. A sockets connection is attempted in the following order:

<ul>
<li>If 
<i>lpszUrl</i> is non-<b>NULL</b>, the host value is extracted from it and used to ping that specific host.</li>
<li>If 
<i>lpszUrl</i> is <b>NULL</b> and there is an entry in the internal server database for the nearest server, the host value is extracted from the entry and used to ping that server.</li>
</ul>

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if a connection is made successfully, or <b>FALSE</b> otherwise. Use 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to retrieve the error code. ERROR_NOT_CONNECTED is returned by 
<b>GetLastError</b> if a connection cannot be made or if the sockets database is unconditionally offline.

## -remarks

<b>InternetCheckConnection</b> is deprecated. <b>InternetCheckConnection</b> does not work in environments that use a web proxy server to access the Internet. Depending on the environment, use  <a href="/uwp/api/Windows.Networking.Connectivity.NetworkInformation#Windows_Networking_Connectivity_NetworkInformation_GetInternetConnectionProfile_">NetworkInformation.GetInternetConnectionProfile</a> or the <a href="/windows/desktop/NLA/nlm-interfaces">NLM Interfaces</a> to check for Internet access instead.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetCheckConnection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
