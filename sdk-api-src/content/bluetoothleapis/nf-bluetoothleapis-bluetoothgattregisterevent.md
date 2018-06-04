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

# BluetoothGATTRegisterEvent function


## -description


The <b>BluetoothGATTRegisterEvent</b> function registers a routine to be called back during a characteristic value change event on the given characteristic identified by its characteristic handle.


## -parameters




### -param hService [in]

Handle to the service.


### -param EventType [in]

A value from <a href="https://msdn.microsoft.com/library/windows/hardware/hh450849">BTH_LE_GATT_EVENT_TYPE</a>. Currently, only <b>CharacteristicValueChangedEvent</b> is supported.


### -param EventParameterIn [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn385750">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a> structure to pass when the event is triggered.


### -param Callback [in]

The routine to call when the Characteristic value changes.


### -param CallbackContext [in, optional]

Context to pass to <i>Callback</i>.


### -param pEventHandle [out]

Pointer to buffer to receive a handle for the registration.  Profile drivers must pass this handle when calling <a href="https://msdn.microsoft.com/library/windows/hardware/hh450809">BluetoothGATTUnregisterEvent</a>.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn385750">BLUETOOTH_GATT_VALUE_CHANGED_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450849">BTH_LE_GATT_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/96AC4E49-76D7-47B5-93B9-64D574A28E0A">Bluetooth GATT Event Callback Function</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450809">BluetoothGATTUnregisterEvent</a>
 

 

