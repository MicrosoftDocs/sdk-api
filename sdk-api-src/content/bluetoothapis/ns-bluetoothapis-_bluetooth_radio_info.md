---
UID: NS:bluetoothapis._BLUETOOTH_RADIO_INFO
title: "_BLUETOOTH_RADIO_INFO"
author: windows-sdk-content
description: Contains information about a Bluetooth radio.
old-location: bluetooth\bluetooth_radio_info.htm
tech.root: Bluetooth
ms.assetid: 14440e02-ff2e-4fae-aac9-1b2fd936510e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PBLUETOOTH_RADIO_INFO, BLUETOOTH_RADIO_INFO, BLUETOOTH_RADIO_INFO structure [Bluetooth], _BLUETOOTH_RADIO_INFO, bluetooth.bluetooth_radio_info, bluetoothapis/BLUETOOTH_RADIO_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - BLUETOOTH_RADIO_INFO
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_RADIO_INFO, *PBLUETOOTH_RADIO_INFO
req.redist: 
---

# _BLUETOOTH_RADIO_INFO structure


## -description


The <b>BLUETOOTH_RADIO_INFO</b> structure contains information about a Bluetooth radio.


## -struct-fields




### -field dwSize

Size, in bytes,  of the structure.


### -field address

Address of the local Bluetooth radio.


### -field szName

Name of the local Bluetooth radio.


### -field ulClassofDevice

Device class for the local Bluetooth radio.


### -field lmpSubversion

This member contains data specific to individual Bluetooth device manufacturers.


### -field manufacturer

Manufacturer of the Bluetooth radio, expressed as a <b>BTH_MFG_Xxx</b> value. For more information about the Bluetooth assigned numbers document and a current list of values, see the Bluetooth specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362926(v=VS.85).aspx">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362786(v=VS.85).aspx">BluetoothFindFirstRadio</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362790(v=VS.85).aspx">BluetoothFindNextRadio</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362792(v=VS.85).aspx">BluetoothFindRadioClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362797(v=VS.85).aspx">BluetoothGetRadioInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms741580(v=VS.85).aspx">WSAGetLastError</a>
 

 

