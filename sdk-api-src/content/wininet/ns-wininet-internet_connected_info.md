---
UID: NS:wininet.INTERNET_CONNECTED_INFO
title: INTERNET_CONNECTED_INFO (wininet.h)
description: Contains the information to set the global online/offline state.
helpviewer_keywords: ["*LPINTERNET_CONNECTED_INFO","INTERNET_CONNECTED_INFO","INTERNET_CONNECTED_INFO structure [WinINet]","INTERNET_STATE_BUSY","INTERNET_STATE_CONNECTED","INTERNET_STATE_DISCONNECTED","INTERNET_STATE_DISCONNECTED_BY_USER","INTERNET_STATE_IDLE","LPINTERNET_CONNECTED_INFO","LPINTERNET_CONNECTED_INFO structure pointer [WinINet]","_inet_internet_connected_info_structure","wininet.internet_connected_info","wininet/ LPINTERNET_CONNECTED_INFO","wininet/INTERNET_CONNECTED_INFO"]
old-location: wininet\internet_connected_info.htm
tech.root: wininet
ms.assetid: 585dbacb-33b1-4655-9ae3-5dacf30a70da
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_CONNECTED_INFO, INTERNET_CONNECTED_INFO, INTERNET_CONNECTED_INFO structure [WinINet], INTERNET_STATE_BUSY, INTERNET_STATE_CONNECTED, INTERNET_STATE_DISCONNECTED, INTERNET_STATE_DISCONNECTED_BY_USER, INTERNET_STATE_IDLE, LPINTERNET_CONNECTED_INFO, LPINTERNET_CONNECTED_INFO structure pointer [WinINet], _inet_internet_connected_info_structure, wininet.internet_connected_info, wininet/ LPINTERNET_CONNECTED_INFO, wininet/INTERNET_CONNECTED_INFO'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERNET_CONNECTED_INFO, *LPINTERNET_CONNECTED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPINTERNET_CONNECTED_INFO
 - wininet/LPINTERNET_CONNECTED_INFO
 - INTERNET_CONNECTED_INFO
 - wininet/INTERNET_CONNECTED_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_CONNECTED_INFO
---

# INTERNET_CONNECTED_INFO structure


## -description

Contains the information to set the global online/offline state.

## -struct-fields

### -field dwConnectedState

State information. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_CONNECTED"></a><a id="internet_state_connected"></a><dl>
<dt><b>INTERNET_STATE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Connected to network. Replaces INTERNET_STATE_ONLINE. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_DISCONNECTED"></a><a id="internet_state_disconnected"></a><dl>
<dt><b>INTERNET_STATE_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Disconnected from network. Replaces INTERNET_STATE_OFFLINE. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_DISCONNECTED_BY_USER"></a><a id="internet_state_disconnected_by_user"></a><dl>
<dt><b>INTERNET_STATE_DISCONNECTED_BY_USER</b></dt>
</dl>
</td>
<td width="60%">
Disconnected by user request. Replaces INTERNET_STATE_OFFLINE_USER. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_IDLE"></a><a id="internet_state_idle"></a><dl>
<dt><b>INTERNET_STATE_IDLE</b></dt>
</dl>
</td>
<td width="60%">
No network requests are being made. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_BUSY"></a><a id="internet_state_busy"></a><dl>
<dt><b>INTERNET_STATE_BUSY</b></dt>
</dl>
</td>
<td width="60%">
Network requests are being made. 

</td>
</tr>
</table>

### -field dwFlags

Controls the transition between states. This member can be ISO_FORCE_DISCONNECTED, which puts WinINet into offline mode. All outstanding requests will be aborted with a canceled error.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a>

