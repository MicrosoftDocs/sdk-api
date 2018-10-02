---
UID: NF:bluetoothapis.BluetoothDisplayDeviceProperties
title: BluetoothDisplayDeviceProperties function
author: windows-sdk-content
description: Starts Control Panel device information property sheet.
old-location: bluetooth\bluetoothdisplaydeviceproperties.htm
tech.root: Bluetooth
ms.assetid: cb33cf35-eb1e-4953-a779-4eb38afe0c34
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothDisplayDeviceProperties, BluetoothDisplayDeviceProperties function [Bluetooth], bluetooth.bluetoothdisplaydeviceproperties, bluetoothapis/BluetoothDisplayDeviceProperties
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
 - BluetoothDisplayDeviceProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothDisplayDeviceProperties function


## -description


The <b>BluetoothDisplayDeviceProperties</b> function starts Control Panel device information property sheet.


## -parameters




### -param hwndParent

A handle to the parent window of the property sheet.


### -param pbtdi

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> structure that contains information about the Bluetooth device.


## -returns



Returns <b>TRUE</b> if the property sheet is successfully displayed. Returns <b>FALSE</b> if the property sheet was not displayed successfully; call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for additional error information.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362782(v=VS.85).aspx">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362788(v=VS.85).aspx">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362795(v=VS.85).aspx">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362884(v=VS.85).aspx">BluetoothRemoveDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362896(v=VS.85).aspx">BluetoothUpdateDeviceRecord</a>
 

 

