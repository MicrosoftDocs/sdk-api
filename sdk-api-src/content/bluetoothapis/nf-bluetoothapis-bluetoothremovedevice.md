---
UID: NF:bluetoothapis.BluetoothRemoveDevice
title: BluetoothRemoveDevice function
author: windows-sdk-content
description: Removes authentication between a Bluetooth device and the computer and clears cached service information for the device.
old-location: bluetooth\bluetoothremovedevice.htm
tech.root: bluetooth
ms.assetid: dd4f6468-ccc2-4072-95c5-97553308ae47
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: BluetoothRemoveDevice, BluetoothRemoveDevice function [Bluetooth], bluetooth.bluetoothremovedevice, bluetoothapis/BluetoothRemoveDevice
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
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothRemoveDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothRemoveDevice function


## -description


The <b>BluetoothRemoveDevice</b> function removes authentication between a Bluetooth device and the computer and clears cached service information for the device.


## -parameters




### -param pAddress

A pointer to the address of the Bluetooth device to be removed.


## -returns



Returns <b>ERROR_SUCCESS</b> upon successful removal of the Bluetooth device. Returns <b>ERROR_NOT_FOUND</b> if the device was not found.




## -remarks



The <b>BluetoothRemoveDevice</b> function fails if the device indicated by <i>pAddress</i> is not a remembered device.




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>
 

 

