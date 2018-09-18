---
UID: NF:bluetoothleapis.BluetoothGATTBeginReliableWrite
title: BluetoothGATTBeginReliableWrite function
author: windows-sdk-content
description: The BluetoothGATTBeginReliableWrite function specifies that reliable writes are about to begin.
old-location: bltooth\bluetoothgattbeginreliablewrite.htm
tech.root: bltooth
ms.assetid: D053FD0C-3088-4C56-A4EA-F41079FAAF20
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BluetoothGATTBeginReliableWrite, BluetoothGATTBeginReliableWrite function [Bluetooth Devices], bltooth.bluetoothgattbeginreliablewrite, bluetoothleapis/BluetoothGATTBeginReliableWrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bluetoothleapis.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Supported in Windows 8 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: BluetoothAPIs.lib
req.dll: BluetoothAPIs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothGATTBeginReliableWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothGATTBeginReliableWrite function


## -description


The <b>BluetoothGATTBeginReliableWrite</b> function specifies that reliable writes are about to begin.


## -parameters




### -param hDevice [in]

Handle to the service.


### -param ReliableWriteContext [out]

Address of a <b>BTH_LE_GATT_RELIABLE_WRITE_CONTEXT</b> structure containing the context describing the reliable write operation.


### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTBeginReliableWrite</b>:

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>BLUETOOTH_GATT_FLAG_NONE</b>

</td>
<td>
The client does not have specific GATT requirements (default).

</td>
</tr>
</table>
 


## -returns



The <b>BluetoothGATTBeginReliableWrite</b> function returns the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Returned if both a parent service and a service handle are provided and the service hierarchy does not roll up to the provided parent service handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
A reliable write operation is already presently underway.

</td>
</tr>
</table>
 




## -remarks



The <b>BluetoothGATTBeginReliableWrite</b> function notifies the Bluetooth stack that procedures that are to be called after the function returns are reliable write operations.  Any operations that do not support reliable writes will return an <b>ERROR_INVALID_FUNCTION</b> error. Only the following functions support reliable write operations:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh450806(v=VS.85).aspx">BluetoothGATTSetCharacteristicValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh450794(v=VS.85).aspx">BluetoothGATTEndReliableWrite</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh450791(v=VS.85).aspx">BluetoothGATTAbortReliableWrite</a>
</li>
</ul>

#### Examples


```cpp

BTH_LE_GATT_RELIABLE_WRITE_CONTEXT ReliableWriteContext = NULL;
hr = BluetoothGATTBeginReliableWrite(hDevice, 
                                    &ReliableWriteContext,
                                    BLUETOOTH_GATT_FLAG_NONE);

if (SUCCEEDED(hr)) {
    // Calls to BluetoothGATTSetCharacteristicValue
}

if (NULL != ReliableWriteContext) {
    BluetoothGATTEndReliableWrite(hDevice, 
                                 ReliableWriteContext,
                                  BLUETOOTH_GATT_FLAG_NONE);
}
```




