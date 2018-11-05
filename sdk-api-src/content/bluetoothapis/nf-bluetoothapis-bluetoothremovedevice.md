---
UID: NF:bluetoothapis.BluetoothRemoveDevice
title: BluetoothRemoveDevice function
author: windows-sdk-content
description: Removes authentication between a Bluetooth device and the computer and clears cached service information for the device.
old-location: bluetooth\bluetoothremovedevice.htm
tech.root: Bluetooth
ms.assetid: dd4f6468-ccc2-4072-95c5-97553308ae47
ms.author: windowssdkdev
ms.date: 09/26/2018
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




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362774(v=VS.85).aspx">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362782(v=VS.85).aspx">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362788(v=VS.85).aspx">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362795(v=VS.85).aspx">BluetoothGetDeviceInfo</a>
 

 

