---
UID: NF:wininet.InternetDialA
title: InternetDialA function (wininet.h)
description: The InternetDialA (ANSI) function (wininet.h) initiates a connection to the Internet using a modem.
helpviewer_keywords: ["InternetDialA"]
old-location: wininet\internetdial.htm
tech.root: wininet
ms.assetid: b8ce748b-9879-4f68-aea1-32e2bfaee8ab
ms.date: 08/10/2022
ms.keywords: InternetDial, InternetDial function [WinINet], InternetDialA, InternetDialW, _inet_internetdial_function, wininet.internetdial, winineti/InternetDial, winineti/InternetDialA, winineti/InternetDialW
req.header: wininet.h
req.include-header: Wininet.h, Winineti.h, Wininet.h, Winineti.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetDialW (Unicode) and InternetDialA (ANSI)
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
 - InternetDialA
 - wininet/InternetDialA
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
 - InternetDial
 - InternetDialA
 - InternetDialW
---

# InternetDialA function


## -description

Initiates a connection to the Internet using a modem.

## -parameters

### -param hwndParent [in]

Handle to the parent window.

### -param lpszConnectoid [in]

Pointer to a <b>null</b>-terminated string that specifies the name of the dial-up connection to be used. If this parameter contains the empty string (""), the user chooses the connection. If this parameter is <b>NULL</b>, the function connects to the autodial connection.

### -param dwFlags [in]

Options. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_AUTODIAL_FORCE_ONLINE</dt>
</dl>
</td>
<td width="60%">
Forces an online connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_AUTODIAL_FORCE_UNATTENDED</dt>
</dl>
</td>
<td width="60%">
Forces an unattended Internet dial-up. If user intervention is required, the function will fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DIAL_FORCE_PROMPT</dt>
</dl>
</td>
<td width="60%">
Ignores the "dial automatically" setting and forces the dialing user interface to be displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DIAL_UNATTENDED</dt>
</dl>
</td>
<td width="60%">
Connects to the Internet through a modem, without displaying a user interface, if possible. Otherwise, the function will wait for user input.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_DIAL_SHOW_OFFLINE</dt>
</dl>
</td>
<td width="60%">
Shows the <b>Work Offline</b> button instead of the <b>Cancel</b> button in the dialing user interface.

</td>
</tr>
</table>

### -param lpdwConnection [out]

Pointer to a variable that specifies the connection number. This number is a unique identifier for the connection that can be used in other functions, such as <a href="/windows/desktop/api/wininet/nf-wininet-internethangup">InternetHangUp</a>.

### -param dwReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns ERROR_SUCCESS if successful, or an error value otherwise. The error code can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is a problem with the dial-up connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_USER_DISCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The user clicked either the <b>Work Offline</b> or <b>Cancel</b> button on the Internet connection dialog box.

</td>
</tr>
</table>

## -remarks

<b>InternetDial</b> does not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.

<div class="alert"><b>Note</b>  Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the <a href="/windows/desktop/RRAS/remote-access-service-functions">RAS  functions</a> to establish a dial-up connection. WinINet supports the functionality documented in the <a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a> function.</div>
<div> </div>
Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetDial as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/establishing-a-dial-up-connection-to-the-internet">Establishing a Dial-Up Connection to the Internet</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
