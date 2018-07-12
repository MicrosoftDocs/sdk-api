---
UID: NF:wininet.InternetGetConnectedStateEx
title: InternetGetConnectedStateEx function
author: windows-sdk-content
description: Note  Using this API is not recommended, use the INetworkListManager::GetConnectivity method instead. Retrieves the connected state of the specified Internet connection.
old-location: wininet\internetgetconnectedstateex.htm
old-project: wininet
ms.assetid: 0b27b86d-6e55-4022-84ce-d4116d71f124
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: INTERNET_CONNECTION_CONFIGURED, INTERNET_CONNECTION_LAN, INTERNET_CONNECTION_MODEM, INTERNET_CONNECTION_MODEM_BUSY, INTERNET_CONNECTION_OFFLINE, INTERNET_CONNECTION_PROXY, InternetGetConnectedStateEx, InternetGetConnectedStateEx function [WinINet], InternetGetConnectedStateExA, InternetGetConnectedStateExW, _inet_internetgetconnectedstateex_function, wininet.internetgetconnectedstateex, winineti/InternetGetConnectedStateEx, winineti/InternetGetConnectedStateExA, winineti/InternetGetConnectedStateExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: Wininet.h, Winineti.h, Wininet.h, Winineti.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetConnectedStateExW (Unicode) and InternetGetConnectedStateExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetGetConnectedStateEx
 - InternetGetConnectedStateExA
 - InternetGetConnectedStateExW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetGetConnectedStateEx function


## -description


<div class="alert"><b>Note</b>  Using this API is not recommended, use the <a href="https://msdn.microsoft.com/4695554a-2f8b-4d2e-b3ff-ec22c43387d6">INetworkListManager::GetConnectivity</a> method instead.</div><div> </div>Retrieves the connected state of the specified Internet connection.


## -parameters




### -param lpdwFlags [out]

Pointer to a variable that receives the connection description. This parameter may return a valid flag even when the function returns <b>FALSE</b>. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_CONFIGURED"></a><a id="internet_connection_configured"></a><dl>
<dt><b>INTERNET_CONNECTION_CONFIGURED</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Local system has a valid connection to the Internet, but it might or might not be currently connected.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_LAN_"></a><a id="internet_connection_lan_"></a><dl>
<dt><b>INTERNET_CONNECTION_LAN </b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Local system uses a local area network to connect to the Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_MODEM"></a><a id="internet_connection_modem"></a><dl>
<dt><b>INTERNET_CONNECTION_MODEM</b></dt>
<dt> 0x01</dt>
</dl>
</td>
<td width="60%">
Local system uses a modem to connect to the Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_MODEM_BUSY"></a><a id="internet_connection_modem_busy"></a><dl>
<dt><b>INTERNET_CONNECTION_MODEM_BUSY</b></dt>
<dt> 0x08</dt>
</dl>
</td>
<td width="60%">
No longer used.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_OFFLINE_"></a><a id="internet_connection_offline_"></a><dl>
<dt><b>INTERNET_CONNECTION_OFFLINE </b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Local system is in offline mode.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_CONNECTION_PROXY"></a><a id="internet_connection_proxy"></a><dl>
<dt><b>INTERNET_CONNECTION_PROXY</b></dt>
<dt> 0x04</dt>
</dl>
</td>
<td width="60%">
Local system uses a proxy server to connect to the Internet.

</td>
</tr>
</table>
 


### -param lpszConnectionName [out]

Pointer to a string value that receives the connection name.


### -param dwNameLen [in]

Size of the 
<i>lpszConnectionName</i> string, in <b>TCHARs</b>.


### -param dwReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if there is an Internet connection, or <b>FALSE</b> if there is no Internet connection, or if all possible Internet connections are not currently active. For more information, see the Remarks section.

When <a href="https://msdn.microsoft.com/500765b8-fbe4-4bba-894e-cc7f114d9eaa">InternetGetConnectedState</a> returns <b>FALSE</b>, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code.




## -remarks



A return value of <b>TRUE</b> from <a href="https://msdn.microsoft.com/500765b8-fbe4-4bba-894e-cc7f114d9eaa">InternetGetConnectedState</a> indicates that at least one connection to the Internet is available.  It does not guarantee that a connection to a specific host can be established.    Applications should always check for errors returned from API calls that connect to a server. <a href="https://msdn.microsoft.com/4666e4ee-057e-452d-ac2c-d03321a0073f">InternetCheckConnection</a> can be called to determine if a connection to a specific destination can be established.

A return value of <b>TRUE</b> indicates that either the modem connection is active, or a LAN connection is active and a proxy is properly configured for the LAN. A return value of <b>FALSE</b> indicates that neither the modem nor the LAN is connected. If <b>FALSE</b> is returned, the <b>INTERNET_CONNECTION_CONFIGURED</b> flag may be set to indicate that autodial is configured to "always dial" but is not currently active. If autodial is not configured, the function returns <b>FALSE</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dd33ed4b-eb7c-449c-b309-8f5c290a5a93">Establishing a Dial-Up Connection to the Internet</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

