---
UID: NF:bluetoothapis.BluetoothSetLocalServiceInfo
title: BluetoothSetLocalServiceInfo function
author: windows-driver-content
description: Sets local service information for a specific Bluetooth radio.
old-location: bluetooth\bluetoothsetlocalserviceinfo.htm
old-project: Bluetooth
ms.assetid: 836c7804-6747-4a0b-b97c-c8c4e00374ca
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: BluetoothSetLocalServiceInfo, BluetoothSetLocalServiceInfo function [Bluetooth], bluetooth.bluetoothsetlocalserviceinfo, bluetoothapis/BluetoothSetLocalServiceInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	BluetoothSetLocalServiceInfo
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothSetLocalServiceInfo function


## -description



The <b>BluetoothSetLocalServiceInfo</b> function
sets local service information for a specific Bluetooth radio. This function is used to advertise services to which remote devices can connect.<div class="alert"><b>Note</b>  Service information set with this function will persist across reboots.</div>
<div> </div>



## -parameters




### -param hRadioIn [in, optional]

A handle of the Bluetooth radio device to which the local service information applies. If this parameter is <b>NULL</b>, <b>BluetoothSetLocalServiceInfo</b> searches for the first available local Bluetooth radio.


### -param pClassGuid [in]

The GUID of the service to expose. This should match the GUID in the server-side INF file for the profile driver. 


### -param ulInstance

An instance ID for the device node of the Plug and Play (PnP) ID. 


### -param pServiceInfoIn

A pointer to a <a href="https://msdn.microsoft.com/d16fe6f1-4b76-4dbe-825e-e3995d2b4961">BLUETOOTH_LOCAL_SERVICE_INFO</a> structure that describes the local service to set.


## -returns



Returns ERROR_SUCCESS upon successful completion. The following table shows some common errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified Bluetooth radio was not detected. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_UNIT </b></dt>
</dl>
</td>
<td width="60%">
No Bluetooth radios were detected. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There were insufficient resources to complete the operation. This condition occurs when more than 100 local physical device objects (PDOs) corresponding to Bluetooth services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the required privileges.

</td>
</tr>
</table>
 




## -remarks



Applications can call <b>BluetoothSetLocalServiceInfo</b> subsequent times with the same service GUID but with a <b>different</b> instance ID to create multiple instances of the specified server-side profile.
It is important that each instance ID associated with a device is unique,  as it will prevent the service driver from being prematurely uninstalled if one, of possibly many, dependent devices is unpaired.

 The process that calls <b>BluetoothSetLocalServiceInfo</b> must have the <b>SE_LOAD_DRIVER_NAME</b> privilege. A process running in the system or in the  administrator context can elevate its privilege using the <a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a> and <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/d16fe6f1-4b76-4dbe-825e-e3995d2b4961">BLUETOOTH_LOCAL_SERVICE_INFO</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=98686">BluetoothSetLocalServiceInfo (WDK)</a>
 

 

