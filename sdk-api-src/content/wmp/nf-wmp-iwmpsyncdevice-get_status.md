---
UID: NF:wmp.IWMPSyncDevice.get_status
title: IWMPSyncDevice::get_status
author: windows-sdk-content
description: The get_status method retrieves a value that indicates the status of the relationship between Windows Media Player and the device.
old-location: wmp\iwmpsyncdevice_get_status.htm
tech.root: WMP
ms.assetid: 2b194161-c25c-43d9-90ee-dd25ff61034b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_status method, IWMPSyncDevice.get_status, IWMPSyncDevice::get_status, IWMPSyncDeviceget_status, get_status, get_status method [Windows Media Player], get_status method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_status, wmp/IWMPSyncDevice::get_status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMPSyncDevice.get_status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSyncDevice::get_status


## -description



The <b>get_status</b> method retrieves a value that indicates the status of the relationship between Windows Media Player and the device.




## -parameters




### -param pwmpds [out]

Pointer to a <b>WMPDeviceStatus</b> enumeration value indicating the current status.


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



Windows Media Player 10 or later supports up to 16 device partnerships. The Player allows one partnership with one computer for each device. Creating a new partnership destroys any existing partnership with the current device.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563709(v=VS.85).aspx">IWMPSyncDevice Interface</a>



<a href="https://msdn.microsoft.com/c553d495-d8fc-4483-a3dc-6679c6b9d1f1">Retrieving Device Attributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564695(v=VS.85).aspx">WMPDeviceStatus</a>
 

 

