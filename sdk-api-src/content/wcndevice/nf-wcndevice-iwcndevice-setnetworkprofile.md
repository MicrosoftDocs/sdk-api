---
UID: NF:wcndevice.IWCNDevice.SetNetworkProfile
title: IWCNDevice::SetNetworkProfile
author: windows-sdk-content
description: The IWCNDevice::SetNetworkProfile method queues an XML WLAN profile to be provisioned to the device. This method may only be called prior to IWCNDevice::Connect.
old-location: wcn\iwcndevice_setnetworkprofile.htm
tech.root: wcn
ms.assetid: 267aa55a-005d-4db8-9569-f8ee77a15168
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWCNDevice interface [Windows Connect Now],SetNetworkProfile method, IWCNDevice.SetNetworkProfile, IWCNDevice::SetNetworkProfile, SetNetworkProfile, SetNetworkProfile method [Windows Connect Now], SetNetworkProfile method [Windows Connect Now],IWCNDevice interface, wcn.iwcndevice_setnetworkprofile, wcndevice/IWCNDevice::SetNetworkProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.SetNetworkProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

