---
UID: NS:bluetoothapis._BLUETOOTH_DEVICE_INFO
title: BLUETOOTH_DEVICE_INFO_STRUCT (bluetoothapis.h)
author: windows-sdk-content
description: The BLUETOOTH_DEVICE_INFO structure provides information about a Bluetooth device.
old-location: bluetooth\bluetooth_device_info.htm
tech.root: bluetooth
ms.assetid: 41b14980-8217-4948-b084-1f44051d12f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BLUETOOTH_DEVICE_INFO, BLUETOOTH_DEVICE_INFO structure [Bluetooth], BLUETOOTH_DEVICE_INFO_STRUCT, _BLUETOOTH_DEVICE_INFO, _bth_bluetooth_device_info, bluetooth.bluetooth_device_info, bluetoothapis/BLUETOOTH_DEVICE_INFO
ms.topic: struct
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_DEVICE_INFO
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_DEVICE_INFO_STRUCT
req.redist: 
ms.custom: 19H1
---

# BLUETOOTH_DEVICE_INFO_STRUCT structure


## -description


The 
<b>BLUETOOTH_DEVICE_INFO</b> structure provides information about a Bluetooth device.


## -struct-fields




### -field dwSize

Size of the 
<b>BLUETOOTH_DEVICE_INFO</b> structure, in bytes.


### -field Address

Address of the device.


### -field ulClassofDevice

Class of the device.


### -field fConnected

Specifies whether the device is connected.


### -field fRemembered

Specifies whether the device is a remembered device. Not all remembered devices are authenticated.


### -field fAuthenticated

Specifies whether the device is authenticated, paired, or bonded. All authenticated devices are remembered.


### -field stLastSeen

Last time the device was seen, in the form of a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


### -field stLastUsed

Last time the device was used, in the form of a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


### -field szName

Name of the device.


## -remarks



See the Bluetooth specification at 
<a href="https://www.bluetooth.org/Technical/AssignedNumbers/references.htm">https://www.bluetooth.org/Technical/AssignedNumbers/references.htm</a> for class of device (COD) information.




## -see-also




<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

