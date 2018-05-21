---
UID: NF:bluetoothapis.BluetoothAuthenticateMultipleDevices
title: BluetoothAuthenticateMultipleDevices function
author: windows-driver-content
description: Enables the caller to prompt for multiple devices to be authenticated during a single instance of the Bluetooth Connection wizard.
old-location: bluetooth\bluetoothauthenticatemultipledevices.htm
old-project: Bluetooth
ms.assetid: 81dd4925-7f0a-468f-b706-244ce99e91df
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: BluetoothAuthenticateMultipleDevices, BluetoothAuthenticateMultipleDevices function [Bluetooth], bluetooth.bluetoothauthenticatemultipledevices, bluetoothapis/BluetoothAuthenticateMultipleDevices
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
api_name:
-	BluetoothAuthenticateMultipleDevices
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothAuthenticateMultipleDevices function


## -description


The <b>BluetoothAuthenticateMultipleDevices</b> function enables the caller to prompt for multiple devices to be authenticated during a single instance of the Bluetooth Connection wizard.<div class="alert"><b>Note</b>  <b>BluetoothAuthenticateMultipleDevices</b> has been deprecated. Implementation of this API is not recommended. </div>
<div> </div>



## -parameters




### -param hwndParent

A window to be the parent of the Authentication wizard. If set to <b>NULL</b>, the wizard is parented off the desktop.


### -param hRadio

The valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, authentication is attempted on all local radios; if any radio succeeds, the function call succeeds.


### -param cDevices

The number of devices in the <i>pbtdi</i> array of <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structures.


### -param rgbtdi

TBD




#### - pbtdi

An array of <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structures that contain records for the Bluetooth devices to be authenticated.


## -returns



Returns <b>ERROR_SUCCESS</b> upon successful completion; check the <b>fAuthenticate</b> flag for each device.

The following table  lists common errors.

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
The user canceled the operation. Check the <b>fAuthenticate</b> flag for each Bluetooth device to determine whether any devices were authenticated before the user canceled the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the devices in the <i>pbtdi</i> array was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
All  devices pointed to by <i>pbtdi</i>  are already marked as authenticated.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/8f9c133e-e647-45c8-b2c6-372b18345637">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/e20ad938-cab4-4017-95bf-8d6843f048eb">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

