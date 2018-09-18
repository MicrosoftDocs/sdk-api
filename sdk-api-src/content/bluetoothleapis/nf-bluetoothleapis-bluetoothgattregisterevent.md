---
UID: NF:bluetoothleapis.BluetoothGATTRegisterEvent
title: BluetoothGATTRegisterEvent function
author: windows-sdk-content
description: Registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle.
old-location: bltooth\bluetoothgattregisterevent.htm
tech.root: bltooth
ms.assetid: 8C1477F8-8342-4405-8FE1-8109E6147EE9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BluetoothGATTRegisterEvent, BluetoothGATTRegisterEvent function [Bluetooth Devices], bltooth.bluetoothgattregisterevent, bluetoothleapis/BluetoothGATTRegisterEvent
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
req.lib: BluetoothApis.lib
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
 - BluetoothGATTRegisterEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothGATTRegisterEvent function


## -description


The <b>BluetoothGATTRegisterEvent</b> function registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle.


## -parameters




### -param hService [in]

Handle to the service.


### -param EventType [in]

A value from <a href="https://msdn.microsoft.com/6AF30DEA-2018-4AA2-B13A-BD31BD641F9F">BTH_LE_GATT_EVENT_TYPE</a>. Currently, only <b>CharacteristicValueChangedEvent</b> is supported.


### -param EventParameterIn [in]

Pointer to a <a href="https://msdn.microsoft.com/97EB32A7-87BF-4DBA-9480-4BB7DFCBFB23">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a> structure to pass when the event is triggered.


### -param Callback [in]

The routine to call when the Characteristic value changes.


### -param CallbackContext [in, optional]

Context to pass to <i>Callback</i>.


### -param pEventHandle [out]

Pointer to buffer to receive a handle for the registration.  Profile drivers must pass this handle when calling <a href="https://msdn.microsoft.com/4E0E8D6C-DC12-4F15-9D29-B38AE680894B">BluetoothGATTUnregisterEvent</a>.


### -param Flags [in]

Flags to modify the behavior of <b>BluetoothGATTRegisterEvent</b>:

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



<b>BluetoothGATTRegisterEvent</b> returns the following values:

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter was invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/97EB32A7-87BF-4DBA-9480-4BB7DFCBFB23">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/6AF30DEA-2018-4AA2-B13A-BD31BD641F9F">BTH_LE_GATT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/96AC4E49-76D7-47B5-93B9-64D574A28E0A">Bluetooth GATT Event Callback Function</a>



<a href="https://msdn.microsoft.com/4E0E8D6C-DC12-4F15-9D29-B38AE680894B">BluetoothGATTUnregisterEvent</a>
 

 

