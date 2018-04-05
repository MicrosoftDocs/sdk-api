---
UID: NF:bluetoothapis.BluetoothUpdateDeviceRecord
title: BluetoothUpdateDeviceRecord function
author: windows-driver-content
description: Updates the local computer cache about a Bluetooth device.
old-location: bluetooth\bluetoothupdatedevicerecord.htm
old-project: Bluetooth
ms.assetid: afcf6708-1c2a-43ac-8e5e-1bd0ce7456fc
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: BluetoothUpdateDeviceRecord, BluetoothUpdateDeviceRecord function [Bluetooth], bluetooth.bluetoothupdatedevicerecord, bluetoothapis/BluetoothUpdateDeviceRecord
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
-	BluetoothUpdateDeviceRecord
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothUpdateDeviceRecord function


## -description


The <b>BluetoothUpdateDeviceRecord</b> function updates the local computer cache about a Bluetooth device.


## -parameters




### -param pbtdi

A pointer to the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure to update. For more information, see the Remarks section.


## -returns



Returns <b>ERROR_SUCCESS</b> upon success. The following table  lists common errors.

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
The <i>pbtdi</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the structure pointed to in the <i>pbtdi</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



When updating a Bluetooth device record, the requirements for members of the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure, listed in the following table, must be observed.<table>
<tr>
<th>Member</th>
<th>Requirement</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Must match the structure size.</td>
</tr>
<tr>
<td><b>Address</b></td>
<td>Must be a previously found radio address.</td>
</tr>
<tr>
<td><b>szName</b></td>
<td>Must contain the new name to be stored.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/e267df61-d0f5-434f-b49c-6899c2abfa2a">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>
 

 

