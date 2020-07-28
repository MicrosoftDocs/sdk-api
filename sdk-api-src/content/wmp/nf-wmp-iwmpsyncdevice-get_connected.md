---
UID: NF:wmp.IWMPSyncDevice.get_connected
title: IWMPSyncDevice::get_connected (wmp.h)
description: The get_connected method retrieves a value indicating whether the device is connected to Windows Media Player.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","get_connected method","IWMPSyncDevice.get_connected","IWMPSyncDevice::get_connected","IWMPSyncDeviceget_connected","get_connected","get_connected method [Windows Media Player]","get_connected method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_get_connected","wmp/IWMPSyncDevice::get_connected"]
old-location: wmp\iwmpsyncdevice_get_connected.htm
tech.root: WMP
ms.assetid: c22f4247-8df9-4ac6-ad27-a0e34780b832
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_connected method, IWMPSyncDevice.get_connected, IWMPSyncDevice::get_connected, IWMPSyncDeviceget_connected, get_connected, get_connected method [Windows Media Player], get_connected method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_connected, wmp/IWMPSyncDevice::get_connected
f1_keywords:
- wmp/IWMPSyncDevice.get_connected
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPSyncDevice.get_connected
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice::get_connected


## -description



The <b>get_connected</b> method retrieves a value indicating whether the device is connected to Windows Media Player.




## -parameters




### -param pvbConnected [out]

<b>VARIANT_BOOL</b> indicating whether the device is connected. The following table describes the possible values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The device is connected.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The device is not connected.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/enumerating-devices">Enumerating Devices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/retrieving-device-attributes">Retrieving Device Attributes</a>
 

 

