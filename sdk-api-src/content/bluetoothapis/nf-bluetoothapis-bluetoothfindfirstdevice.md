---
UID: NF:bluetoothapis.BluetoothFindFirstDevice
title: BluetoothFindFirstDevice function
author: windows-driver-content
description: The BluetoothFindFirstDevice function begins the enumeration Bluetooth devices.
old-location: bluetooth\bluetoothfindfirstdevice.htm
old-project: Bluetooth
ms.assetid: f73acbb4-119f-4a73-a338-d11e8cf7e6be
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: BluetoothFindFirstDevice, BluetoothFindFirstDevice function [Bluetooth], bluetooth.bluetoothfindfirstdevice, bluetoothapis/BluetoothFindFirstDevice
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
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
-	BluetoothAPIs.dll
-	Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
-	BluetoothFindFirstDevice
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothFindFirstDevice function


## -description


The <b>BluetoothFindFirstDevice</b> function begins the enumeration Bluetooth devices.


## -parameters




### -param pbtsp

Pointer to a <a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">BLUETOOTH_DEVICE_SEARCH_PARAMS</a> structure. The <b>dwSize</b> member of the <b>BLUETOOTH_DEVICE_SEARCH_PARAMS</b> structure pointed to by <i>pbtsp</i> must match the size of the structure.


### -param pbtdi

Pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure into which information about the first Bluetooth device found is placed. The <b>dwSize</b> member of the <b>BLUETOOTH_DEVICE_INFO</b> structure pointed to by <i>pbtdi</i> must match the size of the structure, or the call to the <b>BluetoothFindFirstDevice</b> function fails.


## -returns



Returns a valid handle to the first Bluetooth device upon successful completion, and the <i>pbtdi</i> parameter points to information about the device. When this handle is no longer needed, it must be closed via the <a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>.

Returns <b>NULL</b> upon failure. Call the  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information on the error. The following table  describe common errors:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbtsp</i> or <i>pbtdi</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The structure pointed to by <i>pbtsp</i> or <i>pbtdi</i> is not the correct size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">
				BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>



<a href="https://msdn.microsoft.com/afcf6708-1c2a-43ac-8e5e-1bd0ce7456fc">BluetoothUpdateDeviceRecord</a>
 

 

