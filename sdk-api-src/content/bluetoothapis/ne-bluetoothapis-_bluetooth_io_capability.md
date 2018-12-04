---
UID: NE:bluetoothapis._BLUETOOTH_IO_CAPABILITY
title: "_BLUETOOTH_IO_CAPABILITY"
author: windows-sdk-content
description: BLUETOOTH_IO_CAPABILITY enumeration defines the input/output capabilities of a Bluetooth Device.
old-location: bluetooth\bluetooth_io_capability.htm
tech.root: Bluetooth
ms.assetid: f1cd4fc9-5206-4f38-a2b9-621ca4c6ab86
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BLUETOOTH_IO_CAPABILITY, BLUETOOTH_IO_CAPABILITY enumeration [Bluetooth], BLUETOOTH_IO_CAPABILITY_DISPLAYONLY, BLUETOOTH_IO_CAPABILITY_DISPLAYYESNO, BLUETOOTH_IO_CAPABILITY_KEYBOARDONLY, BLUETOOTH_IO_CAPABILITY_NOINPUTNOOUTPUT, BLUETOOTH_IO_CAPABILITY_UNDEFINED, _BLUETOOTH_IO_CAPABILITY, bluetooth.bluetooth_io_capability, bluetoothapis/BLUETOOTH_IO_CAPABILITY, bluetoothapis/BLUETOOTH_IO_CAPABILITY_DISPLAYONLY, bluetoothapis/BLUETOOTH_IO_CAPABILITY_DISPLAYYESNO, bluetoothapis/BLUETOOTH_IO_CAPABILITY_KEYBOARDONLY, bluetoothapis/BLUETOOTH_IO_CAPABILITY_NOINPUTNOOUTPUT, bluetoothapis/BLUETOOTH_IO_CAPABILITY_UNDEFINED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - BLUETOOTH_IO_CAPABILITY
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_IO_CAPABILITY
req.redist: 
---

# _BLUETOOTH_IO_CAPABILITY enumeration


## -description


The <b>BLUETOOTH_IO_CAPABILITY</b> enumeration defines the input/output capabilities of a Bluetooth Device.


## -enum-fields




### -field BLUETOOTH_IO_CAPABILITY_DISPLAYONLY

The Bluetooth device is capable of output via display only.


### -field BLUETOOTH_IO_CAPABILITY_DISPLAYYESNO

The Bluetooth device is capable of output via a display, and has the additional capability to presenting a yes/no question to the user.


### -field BLUETOOTH_IO_CAPABILITY_KEYBOARDONLY

The Bluetooth device is capable of input via keyboard.


### -field BLUETOOTH_IO_CAPABILITY_NOINPUTNOOUTPUT

The Bluetooth device is not capable of input/output.


### -field BLUETOOTH_IO_CAPABILITY_UNDEFINED

The input/output capabilities for the Bluetooth device are undefined.


## -see-also




<a href="https://msdn.microsoft.com/fc7eda84-3e7b-49e9-a1a6-e1759c894e1a">BLUETOOTH_AUTHENTICATE_RESPONSE</a>
 

 

