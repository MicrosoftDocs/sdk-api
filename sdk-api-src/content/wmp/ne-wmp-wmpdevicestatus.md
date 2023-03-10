---
UID: NE:wmp.WMPDeviceStatus
title: WMPDeviceStatus (wmp.h)
description: The WMPDeviceStatus enumeration type defines the possible values for the current status of a device. To use this enumeration, you must create a remoted instance of the Windows Media Player 10 or later control.
helpviewer_keywords: ["WMPDeviceStatus","WMPDeviceStatus enumeration [Windows Media Player]","wmp.wmpdevicestatus","wmp/WMPDeviceStatus","wmp/wmpdsLast","wmp/wmpdsManualDevice","wmp/wmpdsNewDevice","wmp/wmpdsPartnershipAnother","wmp/wmpdsPartnershipDeclined","wmp/wmpdsPartnershipExists","wmp/wmpdsUnknown","wmpdsLast","wmpdsManualDevice","wmpdsNewDevice","wmpdsPartnershipAnother","wmpdsPartnershipDeclined","wmpdsPartnershipExists","wmpdsUnknown"]
old-location: wmp\wmpdevicestatus.htm
tech.root: WMP
ms.assetid: dbbb97f8-4b26-4add-a661-a48eff8ad0f5
ms.date: 12/05/2018
ms.keywords: WMPDeviceStatus, WMPDeviceStatus enumeration [Windows Media Player], wmp.wmpdevicestatus, wmp/WMPDeviceStatus, wmp/wmpdsLast, wmp/wmpdsManualDevice, wmp/wmpdsNewDevice, wmp/wmpdsPartnershipAnother, wmp/wmpdsPartnershipDeclined, wmp/wmpdsPartnershipExists, wmp/wmpdsUnknown, wmpdsLast, wmpdsManualDevice, wmpdsNewDevice, wmpdsPartnershipAnother, wmpdsPartnershipDeclined, wmpdsPartnershipExists, wmpdsUnknown
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
targetos: Windows
req.typenames: WMPDeviceStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPDeviceStatus
 - wmp/WMPDeviceStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPDeviceStatus
---

# WMPDeviceStatus enumeration


## -description

The <b>WMPDeviceStatus</b> enumeration type defines the possible values for the current status of a device. To use this enumeration, you must create a remoted instance of the Windows Media Player 10 or later control.

## -enum-fields

### -field wmpdsUnknown:0

Not a valid status.

### -field wmpdsPartnershipExists

A partnership between Windows Media Player and the device exists.

### -field wmpdsPartnershipDeclined

The user declined to create a partnership with the device. A device will also have this status when the partnership was deleted programmatically by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership">IWMPSyncDevice::deletePartnership</a>.

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

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicestatuschange">IWMPEvents2::DeviceStatusChange</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status">IWMPSyncDevice::get_status</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
