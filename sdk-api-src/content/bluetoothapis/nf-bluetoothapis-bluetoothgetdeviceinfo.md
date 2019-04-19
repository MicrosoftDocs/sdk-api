---
UID: NF:bluetoothapis.BluetoothGetDeviceInfo
title: BluetoothGetDeviceInfo function (bluetoothapis.h)
author: windows-sdk-content
description: Retrieves information about a remote Bluetooth device.
old-location: bluetooth\bluetoothgetdeviceinfo.htm
tech.root: bluetooth
ms.assetid: 530e5131-a0ab-4ddd-be73-a07f94e74f73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BluetoothGetDeviceInfo, BluetoothGetDeviceInfo function [Bluetooth], bluetooth.bluetoothgetdeviceinfo, bluetoothapis/BluetoothGetDeviceInfo
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
 - BluetoothGetDeviceInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BluetoothGetDeviceInfo function


## -description


The <b>BluetoothGetDeviceInfo</b> function retrieves information about a remote Bluetooth device. The Bluetooth device must have been previously identified through a successful device inquiry function call.


## -parameters




### -param hRadio

A handle to a local radio, obtained from a call to the <a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a> or similar functions, or from a call to the <b>SetupDiEnumerateDeviceInterfaces</b> function.


### -param pbtdi

A pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure into which data about the first Bluetooth device will be placed. For more information, see Remarks.


## -returns



Returns <b>ERROR_SUCCESS</b> upon success, indicating that data about the remote Bluetooth device was retrieved. Returns error codes upon failure. The following table lists common error codes associated with the <b>BluetoothGetDeviceInfo</b> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The size of the BLUETOOTH_DEVICE_INFO is not compatible. Check
the <b>dwSize</b> member of the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The radio is not known by the system, or the <b>Address</b> member of the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure is all zeros.

</td>
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
</table>
 




## -remarks



The Bluetooth device for which data is obtained must have been previously identified through a successful device inquiry function call.

In the <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure pointed to by <i>pbtdi</i>, the  <b>dwSize</b> member must be equivalent to the size, in bytes, of the structure. The <b>Address</b>          member of the <b>BLUETOOTH_DEVICE_INFO</b> structure must contain the Bluetooth address of the remote
device.




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>
 

 

