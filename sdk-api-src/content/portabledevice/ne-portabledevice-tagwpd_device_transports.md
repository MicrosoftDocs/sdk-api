---
UID: NE:portabledevice.tagWPD_DEVICE_TRANSPORTS
title: tagWPD_DEVICE_TRANSPORTS
author: windows-driver-content
description: The WPD_DEVICE_TRANSPORTS enumeration type specifies the inheritance relationship for a service. This enumeration is used by the WPD_DEVICE_TRANSPORT property.
old-location: wpdsdk\wpd_device_transports.htm
old-project: wpd_sdk
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_DEVICE_TRANSPORTS, WPD_DEVICE_TRANSPORTS enumeration [Windows Portable Devices SDK], WPD_DEVICE_TRANSPORT_BLUETOOTH, WPD_DEVICE_TRANSPORT_IP, WPD_DEVICE_TRANSPORT_UNSPECIFIED, WPD_DEVICE_TRANSPORT_USB, portabledevice/WPD_DEVICE_TRANSPORTS, portabledevice/WPD_DEVICE_TRANSPORT_BLUETOOTH, portabledevice/WPD_DEVICE_TRANSPORT_IP, portabledevice/WPD_DEVICE_TRANSPORT_UNSPECIFIED, portabledevice/WPD_DEVICE_TRANSPORT_USB, tagWPD_DEVICE_TRANSPORTS, wpdsdk.wpd_device_transports
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_DEVICE_TRANSPORTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_DEVICE_TRANSPORTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_DEVICE_TRANSPORTS enumeration


## -description


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597866">WPD_DEVICE_TRANSPORTS</a> enumeration type specifies the inheritance relationship for a service. This enumeration is used by the <b>WPD_DEVICE_TRANSPORT</b> property.


## -enum-fields




### -field WPD_DEVICE_TRANSPORT_UNSPECIFIED

The transport type was not specified.


### -field WPD_DEVICE_TRANSPORT_USB

The device is connected through USB.


### -field WPD_DEVICE_TRANSPORT_IP

The device is connected through Internet Protocol (IP).


### -field WPD_DEVICE_TRANSPORT_BLUETOOTH

The device is connected through Bluetooth.

