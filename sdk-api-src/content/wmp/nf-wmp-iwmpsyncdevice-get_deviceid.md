---
UID: NF:wmp.IWMPSyncDevice.get_deviceId
title: IWMPSyncDevice::get_deviceId
author: windows-sdk-content
description: The get_deviceId method retrieves the device identifier string.
old-location: wmp\iwmpsyncdevice_get_deviceid.htm
old-project: WMP
ms.assetid: 36d40dc4-5641-49dd-9ef4-31d2acd0f41d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_deviceId method, IWMPSyncDevice.get_deviceId, IWMPSyncDevice::get_deviceId, IWMPSyncDeviceget_deviceId, get_deviceId, get_deviceId method [Windows Media Player], get_deviceId method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_deviceid, wmp/IWMPSyncDevice::get_deviceId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSyncDevice.get_deviceId
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncDevice::get_deviceId


## -description



The <b>get_deviceId</b> method retrieves the device identifier string.




## -parameters




### -param pbstrDeviceId [out]

Address of a <b>BSTR</b> variable that receives a string containing the device identifier.


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



The device identifier is the serial number for the device. This value is not guaranteed to be unique for mass storage devices. However, it is unlikely that a particular user will encounter duplicate serial numbers.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/a7f04b97-8a09-4feb-b776-649aa9d6f407">IWMPSyncDevice::get_partnershipIndex</a>



<a href="https://msdn.microsoft.com/c553d495-d8fc-4483-a3dc-6679c6b9d1f1">Retrieving Device Attributes</a>
 

 

