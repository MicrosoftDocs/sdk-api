---
UID: NF:bluetoothapis.BluetoothSelectDevices
title: BluetoothSelectDevices function
author: windows-sdk-content
description: Enables Bluetooth device selection.
old-location: bluetooth\bluetoothselectdevices.htm
tech.root: Bluetooth
ms.assetid: 97fcbd72-99d5-4c5b-bf16-75eea97cbc77
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothSelectDevices, BluetoothSelectDevices function [Bluetooth], _bth_bluetoothselectdevices, bluetooth.bluetoothselectdevices, bluetoothapis/BluetoothSelectDevices
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
 - BluetoothSelectDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothSelectDevices function


## -description


The 
<b>BluetoothSelectDevices</b> function enables Bluetooth device selection.


## -parameters




### -param pbtsdp

A pointer to a 
<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure that identifies Bluetooth devices.


## -returns



Returns <b>TRUE</b> if a user selected a device.

Returns <b>FALSE</b> if no valid data was returned. Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to retrieve error information. The following conditions apply to returned error information.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbtsdp</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The structure passed in <i>pbtsdp</i> is of unknown size.

</td>
</tr>
</table>
 




## -remarks



The <b>BluetoothSelectDevices</b> function opens a common dialog box for selecting Bluetooth devices. The list of devices displayed to the user is determined by the flags and settings the caller specifies in the <i>pbtsdp</i> parameter.

If 
<b>BluetoothSelectDevices</b> returns <b>TRUE</b>, the <b>pDevices</b> member of the 
<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a> structure points to valid data. The caller should verify that  the <b>fAuthenticated</b> and <b>fRemembered</b> flags in the 
<b>BLUETOOTH_SELECT_DEVICE_PARAMS</b> structure to determine which devices were successfully authenticated, and which devices are valid selections for the user. Call the 
<b>BluetoothSelectDevicesFree</b> function to free resources only if the 
<b>BluetoothSelectDevices</b> function returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/8a2bf4dc-43c3-49c0-8ce0-d14ab9f4ae97">PFN_DEVICE_CALLBACK</a>
 

 

