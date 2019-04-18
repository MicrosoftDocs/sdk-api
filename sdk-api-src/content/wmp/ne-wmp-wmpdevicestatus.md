---
UID: NE:wmp.WMPDeviceStatus
title: WMPDeviceStatus (wmp.h)
author: windows-sdk-content
description: The WMPDeviceStatus enumeration type defines the possible values for the current status of a device. To use this enumeration, you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\wmpdevicestatus.htm
tech.root: WMP
ms.assetid: dbbb97f8-4b26-4add-a661-a48eff8ad0f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPDeviceStatus, WMPDeviceStatus enumeration [Windows Media Player], wmp.wmpdevicestatus, wmp/WMPDeviceStatus, wmp/wmpdsLast, wmp/wmpdsManualDevice, wmp/wmpdsNewDevice, wmp/wmpdsPartnershipAnother, wmp/wmpdsPartnershipDeclined, wmp/wmpdsPartnershipExists, wmp/wmpdsUnknown, wmpdsLast, wmpdsManualDevice, wmpdsNewDevice, wmpdsPartnershipAnother, wmpdsPartnershipDeclined, wmpdsPartnershipExists, wmpdsUnknown
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPDeviceStatus
product: Windows
targetos: Windows
req.typenames: WMPDeviceStatus
req.redist: 
ms.custom: 19H1
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

The user declined to create a partnership with the device. A device will also have this status when the partnership was deleted programmatically by calling <a href="https://msdn.microsoft.com/en-us/library/Dd563717(v=VS.85).aspx">IWMPSyncDevice::deletePartnership</a>.


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




<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563293(v=VS.85).aspx">IWMPEvents2::DeviceStatusChange</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563741(v=VS.85).aspx">IWMPSyncDevice::get_status</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

