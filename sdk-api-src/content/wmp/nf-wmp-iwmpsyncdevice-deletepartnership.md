---
UID: NF:wmp.IWMPSyncDevice.deletePartnership
title: IWMPSyncDevice::deletePartnership
author: windows-sdk-content
description: The deletePartnership method terminates the partnership between Windows Media Player and the device.
old-location: wmp\iwmpsyncdevice_deletepartnership.htm
tech.root: WMP
ms.assetid: ecb525b4-c804-47e6-8d6c-7d943010077a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],deletePartnership method, IWMPSyncDevice.deletePartnership, IWMPSyncDevice::deletePartnership, IWMPSyncDevicedeletePartnership, deletePartnership, deletePartnership method [Windows Media Player], deletePartnership method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_deletepartnership, wmp/IWMPSyncDevice::deletePartnership
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
 - IWMPSyncDevice.deletePartnership
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSyncDevice::deletePartnership


## -description



The <b>deletePartnership</b> method terminates the partnership between Windows Media Player and the device.




## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but there was no partnership to delete. This occurs when the current status is wmpdsPartnershipDeclined or wmpdsNewDevice.

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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_MANUALDEVICE (0xC00D1183)</b></dt>
</dl>
</td>
<td width="60%">
The status for the current device is wmpdsManualDevice.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_PARTNERSHIPNOTEXIST (0xC00D1184)</b></dt>
</dl>
</td>
<td width="60%">
The method failed because the current status for the device is wmpdsPartnershipAnother. This method will only delete partnerships that exist for the current instance of Windows Media Player.

</td>
</tr>
</table>
 




## -remarks



When the partnership is deleted, the device status is set to <b>wmpdsPartnershipDeclined</b>. If no partnership exists, this method simply returns S_OK.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice Interface</a>
 

 

