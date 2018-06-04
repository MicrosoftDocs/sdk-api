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
 

 

