---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450806">BluetoothGATTSetCharacteristicValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450794">BluetoothGATTEndReliableWrite</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450791">BluetoothGATTAbortReliableWrite</a>
</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BTH_LE_GATT_RELIABLE_WRITE_CONTEXT ReliableWriteContext = NULL;
hr = BluetoothGATTBeginReliableWrite(hDevice, 
                                    &amp;ReliableWriteContext,
                                    BLUETOOTH_GATT_FLAG_NONE);

if (SUCCEEDED(hr)) {
    // Calls to BluetoothGATTSetCharacteristicValue
}

if (NULL != ReliableWriteContext) {
    BluetoothGATTEndReliableWrite(hDevice, 
                                 ReliableWriteContext,
                                  BLUETOOTH_GATT_FLAG_NONE);
}</pre>
</td>
</tr>
</table></span></div>


