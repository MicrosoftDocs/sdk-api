---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WinHttpGetIEProxyConfigForCurrentUser function


## -description


The <b>WinHttpGetIEProxyConfigForCurrentUser</b> function retrieves the Internet Explorer proxy configuration for the current user.


## -parameters




### -param pProxyConfig [in, out]

A pointer, on input, to a <a href="https://msdn.microsoft.com/b5aebbfe-18c8-4aeb-a01b-488e37d227a1">WINHTTP_CURRENT_USER_IE_PROXY_CONFIG</a> structure. On output, the structure contains the Internet Explorer proxy settings for the current active network connection (for example, LAN, dial-up, or VPN connection).


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No Internet Explorer proxy settings can be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>
 




## -remarks



In Internet Explorer, the proxy settings are found on the <b>Connections</b> tab of the <b>Tools</b> / <b>Internet Options</b> menu option. Proxy settings are configured on a per-connection basis; that is, the proxy settings for a LAN connection are separate from those for a dial-up or VPN connection. <b>WinHttpGetIEProxyConfigForCurrentUser</b> returns the proxy settings for the current active connection.

This function is useful in client applications running in network environments in which the Web Proxy Auto-Discovery (WPAD) protocol is not implemented (meaning that no Proxy Auto-Configuration file is available). If a PAC file is not available, then the <a href="https://msdn.microsoft.com/d01b101e-a496-4e84-9aec-61afe3920fbb">WinHttpGetProxyForUrl</a> function fails. The <b>WinHttpGetIEProxyConfigForCurrentUser</b> function can be used as a fall-back mechanism to discover a workable proxy configuration by retrieving the user's proxy configuration in Internet Explorer.

This function should not be used in a service process that does not impersonate a logged-on user.If the caller does not impersonate a logged on user, WinHTTP attempts to retrieve the Internet Explorer settings for the current service process: for example, the local service or the network service. If the Internet Explorer settings are not configured for these system accounts, the call to <b>WinHttpGetIEProxyConfigForCurrentUser</b> will fail.

The caller must free the <b>lpszProxy</b>, <b>lpszProxyBypass</b>  and <b>lpszAutoConfigUrl</b> strings in the <a href="https://msdn.microsoft.com/b5aebbfe-18c8-4aeb-a01b-488e37d227a1">WINHTTP_CURRENT_USER_IE_PROXY_CONFIG</a>  structure if they are non-<b>NULL</b>. Use <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> to free the strings.




## -see-also




<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP Versions</a>
 

 

