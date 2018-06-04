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

# WMPDeviceStatus enumeration


## -description



The <b>WMPDeviceStatus</b> enumeration type defines the possible values for the current status of a device. To use this enumeration, you must create a remoted instance of the Windows Media Player 10 or later control.




## -enum-fields




### -field wmpdsUnknown

Not a valid status.


### -field wmpdsPartnershipExists

A partnership between Windows Media Player and the device exists.


### -field wmpdsPartnershipDeclined

The user declined to create a partnership with the device. A device will also have this status when the partnership was deleted programmatically by calling <a href="https://msdn.microsoft.com/ecb525b4-c804-47e6-8d6c-7d943010077a">IWMPSyncDevice::deletePartnership</a>.


### -field wmpdsPartnershipAnother

A partnership exists with another computer or user. Windows Media Player 10 or later allows one partnership with one computer per device.


### -field wmpdsManualDevice

The current device supports manual transfers only.


### -field wmpdsNewDevice

The device is a new device; Windows Media Player has information stored for the device.


### -field wmpdsLast

Last enumerated value. Not a valid device state.


## -remarks




          Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/f9781dde-e813-4e2d-820d-5a0803bfbe4e">IWMPEvents2::DeviceStatusChange</a>



<a href="https://msdn.microsoft.com/2b194161-c25c-43d9-90ee-dd25ff61034b">IWMPSyncDevice::get_status</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

