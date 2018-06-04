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

# IWCNDevice::SetNetworkProfile


## -description


The <b>IWCNDevice::SetNetworkProfile</b> method queues an XML WLAN profile to be provisioned to the device.  This method may  only be called prior to <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a>.


## -parameters




### -param pszProfileXml [in]

The XML WLAN profile XML string.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The attribute was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The WLAN profile is not supported for WCN connections.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BAD_PROFILE)</b></dt>
</dl>
</td>
<td width="60%">
The provided XML profile cannot be read.

</td>
</tr>
</table>
 




## -remarks



Currently, the <b>Windows Connect Now API</b> (WCNAPI) supports the following profile types: <ul>
<li>None (Open or Shared)</li>
<li>WEP (Open or Shared)</li>
<li>WPA-PSK (TKIP or AES)</li>
<li>WPA2-PSK (TKIP or AES)</li>
</ul>   If  the specified WLAN profile has extraneous settings (like IHV settings), these settings will be ignored. In the event a WLAN profile is not  compatible with the WCNAPI, an <b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b> value is returned.




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>
 

 

