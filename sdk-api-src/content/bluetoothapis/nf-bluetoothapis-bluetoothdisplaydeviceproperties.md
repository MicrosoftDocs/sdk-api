---
UID: NF:bluetoothapis.BluetoothDisplayDeviceProperties
title: BluetoothDisplayDeviceProperties function
author: windows-sdk-content
description: Starts Control Panel device information property sheet.
old-location: bluetooth\bluetoothdisplaydeviceproperties.htm
old-project: bluetooth
ms.assetid: cb33cf35-eb1e-4953-a779-4eb38afe0c34
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: BluetoothDisplayDeviceProperties, BluetoothDisplayDeviceProperties function [Bluetooth], bluetooth.bluetoothdisplaydeviceproperties, bluetoothapis/BluetoothDisplayDeviceProperties
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BLUETOOTH_IO_CAPABILITY
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
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothDisplayDeviceProperties function


## -description


The <b>BluetoothDisplayDeviceProperties</b> function starts Control Panel device information property sheet.


## -parameters




### -param hwndParent

A handle to the parent window of the property sheet.


### -param pbtdi

A pointer to the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure that contains information about the Bluetooth device.


## -returns



Returns <b>TRUE</b> if the property sheet is successfully displayed. Returns <b>FALSE</b> if the property sheet was not displayed successfully; call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for additional error information.




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>



<a href="https://msdn.microsoft.com/afcf6708-1c2a-43ac-8e5e-1bd0ce7456fc">BluetoothUpdateDeviceRecord</a>
 

 

