---
UID: NF:bluetoothapis.BluetoothSelectDevicesFree
title: BluetoothSelectDevicesFree function
author: windows-sdk-content
description: Frees resources associated with a previous call to BluetoothSelectDevices.
old-location: bluetooth\bluetoothselectdevicesfree.htm
tech.root: Bluetooth
ms.assetid: 9332e62d-a7ee-452e-8e21-27bbbc82448e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothSelectDevicesFree, BluetoothSelectDevicesFree function [Bluetooth], _bth_bluetoothselectdevicesfree, bluetooth.bluetoothselectdevicesfree, bluetoothapis/BluetoothSelectDevicesFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
api_name:
 - BluetoothSelectDevicesFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BluetoothSelectDevicesFree
: 
---

# BluetoothSelectDevicesFree function


## -description


The 
<b>BluetoothSelectDevicesFree</b> function frees resources associated with a previous call to 
<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>.


## -parameters




### -param pbtsdp

A pointer to a 
<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure that identifies the Bluetooth device resources to free.


## -returns



Returns <b>TRUE</b> upon success. Returns <b>FALSE</b> if there are no resources to free.




## -remarks



Only call the <b>BluetoothSelectDevicesFree</b> function if a previous call to the <a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a> function returned <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>
 

 

