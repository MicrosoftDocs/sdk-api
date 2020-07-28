---
UID: NF:wmp.IWMPSyncDevice.get_syncState
title: IWMPSyncDevice::get_syncState (wmp.h)
description: The get_syncState method retrieves a value that indicates the current synchronization state for the device.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","get_syncState method","IWMPSyncDevice.get_syncState","IWMPSyncDevice::get_syncState","IWMPSyncDeviceget_syncState","get_syncState","get_syncState method [Windows Media Player]","get_syncState method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_get_syncstate","wmp/IWMPSyncDevice::get_syncState"]
old-location: wmp\iwmpsyncdevice_get_syncstate.htm
tech.root: WMP
ms.assetid: c93263a1-7976-43db-b514-97d9a263a60c
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],get_syncState method, IWMPSyncDevice.get_syncState, IWMPSyncDevice::get_syncState, IWMPSyncDeviceget_syncState, get_syncState, get_syncState method [Windows Media Player], get_syncState method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_get_syncstate, wmp/IWMPSyncDevice::get_syncState
f1_keywords:
- wmp/IWMPSyncDevice.get_syncState
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
- IWMPSyncDevice.get_syncState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice::get_syncState


## -description



The <b>get_syncState</b> method retrieves a value that indicates the current synchronization state for the device.




## -parameters




### -param pwmpss [out]

Pointer to a <b>WMPSyncState</b> enumeration value indicating the current synchronization state for the device.


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



Devices that have the status <b>wmpdsManualDevice</b> always return wmpssUnknown.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>
 

 

