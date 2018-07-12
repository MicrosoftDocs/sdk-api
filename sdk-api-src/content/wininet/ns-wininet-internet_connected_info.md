---
UID: NS:wininet.INTERNET_CONNECTED_INFO
title: INTERNET_CONNECTED_INFO
author: windows-sdk-content
description: Contains the information to set the global online/offline state.
old-location: wininet\internet_connected_info.htm
old-project: wininet
ms.assetid: 585dbacb-33b1-4655-9ae3-5dacf30a70da
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPINTERNET_CONNECTED_INFO, INTERNET_CONNECTED_INFO, INTERNET_CONNECTED_INFO structure [WinINet], INTERNET_STATE_BUSY, INTERNET_STATE_CONNECTED, INTERNET_STATE_DISCONNECTED, INTERNET_STATE_DISCONNECTED_BY_USER, INTERNET_STATE_IDLE, LPINTERNET_CONNECTED_INFO, LPINTERNET_CONNECTED_INFO structure pointer [WinINet], _inet_internet_connected_info_structure, wininet.internet_connected_info, wininet/ LPINTERNET_CONNECTED_INFO, wininet/INTERNET_CONNECTED_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: INTERNET_CONNECTED_INFO, *LPINTERNET_CONNECTED_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_CONNECTED_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a>
 

 

