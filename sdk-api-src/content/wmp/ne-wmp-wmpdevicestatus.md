---
UID: NE:wmp.WMPDeviceStatus
title: WMPDeviceStatus
author: windows-driver-content
description: The WMPDeviceStatus enumeration type defines the possible values for the current status of a device. To use this enumeration, you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\wmpdevicestatus.htm
old-project: WMP
ms.assetid: dbbb97f8-4b26-4add-a661-a48eff8ad0f5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: WMPDeviceStatus, WMPDeviceStatus enumeration [Windows Media Player], wmp.wmpdevicestatus, wmp/WMPDeviceStatus, wmp/wmpdsLast, wmp/wmpdsManualDevice, wmp/wmpdsNewDevice, wmp/wmpdsPartnershipAnother, wmp/wmpdsPartnershipDeclined, wmp/wmpdsPartnershipExists, wmp/wmpdsUnknown, wmpdsLast, wmpdsManualDevice, wmpdsNewDevice, wmpdsPartnershipAnother, wmpdsPartnershipDeclined, wmpdsPartnershipExists, wmpdsUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WMPDeviceStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wmp.h
api_name:
-	WMPDeviceStatus
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

