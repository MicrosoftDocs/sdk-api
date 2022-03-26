---
UID: NF:bluetoothapis.BluetoothAuthenticateMultipleDevices
title: BluetoothAuthenticateMultipleDevices function (bluetoothapis.h)
description: Enables the caller to prompt for multiple devices to be authenticated during a single instance of the Bluetooth Connection wizard.
helpviewer_keywords: ["BluetoothAuthenticateMultipleDevices","BluetoothAuthenticateMultipleDevices function [Bluetooth]","bluetooth.bluetoothauthenticatemultipledevices","bluetoothapis/BluetoothAuthenticateMultipleDevices"]
old-location: bluetooth\bluetoothauthenticatemultipledevices.htm
tech.root: bluetooth
ms.assetid: 81dd4925-7f0a-468f-b706-244ce99e91df
ms.date: 12/05/2018
ms.keywords: BluetoothAuthenticateMultipleDevices, BluetoothAuthenticateMultipleDevices function [Bluetooth], bluetooth.bluetoothauthenticatemultipledevices, bluetoothapis/BluetoothAuthenticateMultipleDevices
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
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothAuthenticateMultipleDevices
 - bluetoothapis/BluetoothAuthenticateMultipleDevices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
api_name:
 - BluetoothAuthenticateMultipleDevices
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

The number of devices in the <i>pbtdi</i> array of <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structures.

### -param rgbtdi

An array of <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structures that contain records for the Bluetooth devices to be authenticated.

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

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">BluetoothEnableDiscovery</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenableincomingconnections">BluetoothEnableIncomingConnections</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisconnectable">BluetoothIsConnectable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>