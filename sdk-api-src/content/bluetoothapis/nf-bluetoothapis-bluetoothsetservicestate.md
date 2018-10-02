---
UID: NF:bluetoothapis.BluetoothSetServiceState
title: BluetoothSetServiceState function
author: windows-sdk-content
description: Enables or disables services for a Bluetooth device.
old-location: bluetooth\bluetoothsetservicestate.htm
tech.root: Bluetooth
ms.assetid: 9c68139c-6f55-4b5a-bea0-64681e32a7c5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothSetServiceState, BluetoothSetServiceState function [Bluetooth], bluetooth.bluetoothsetservicestate, bluetoothapis/BluetoothSetServiceState
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
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothSetServiceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothSetServiceState function


## -description


The <b>BluetoothSetServiceState</b> function enables or disables services for a Bluetooth device.


## -parameters




### -param hRadio

A handle of the local Bluetooth radio.


### -param pbtdi

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> structure. Must be a previously found radio address.


### -param pGuidService

A pointer to the service GUID on the remote device.


### -param dwServiceFlags

The flags that adjust the service. To disable the service, set to <b>BLUETOOTH_SERVICE_DISABLE</b>; to enable the service, set to <b>BLUETOOTH_SERVICE_ENABLE</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> upon successful completion. The following table  lists common errors.

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
The <i>dwServiceFlags</i> are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The GUID specified in <i>pGuidService</i> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwServiceFlags</i>  is set to <b>BLUETOOTH_SERVICE_DISABLE</b> and the service is already disabled, or <i>dwServiceFlags</i>  is set to  <b>BLUETOOTH_SERVICE_ENABLE</b> and the service is already enabled.

</td>
</tr>
</table>
 




## -remarks



Windows maintains a mapping of  service Globally Unique Identifiers (GUIDs) to supported drivers for
Bluetooth-enabled devices. Enabling a service installs the corresponding
device driver and disabling a service removes the corresponding device driver.
If a non-supported service is enabled, a driver is not installed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362774(v=VS.85).aspx">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362782(v=VS.85).aspx">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362788(v=VS.85).aspx">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362795(v=VS.85).aspx">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362884(v=VS.85).aspx">BluetoothRemoveDevice</a>
 

 

