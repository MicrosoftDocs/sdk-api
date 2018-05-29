---
UID: NF:bluetoothapis.BluetoothAuthenticateDeviceEx
title: BluetoothAuthenticateDeviceEx function
author: windows-sdk-content
description: The BluetoothAuthenticateDeviceEx function sends an authentication request to a remote Bluetooth device.
old-location: bluetooth\bluetoothauthenticatedeviceex.htm
old-project: Bluetooth
ms.assetid: 948bf14c-9661-4fe9-b082-009afd867baf
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothAuthenticateDeviceEx, BluetoothAuthenticateDeviceEx function [Bluetooth], bluetooth.bluetoothauthenticatedeviceex, bluetoothapis/BluetoothAuthenticateDeviceEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
-	BluetoothAuthenticateDeviceEx
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothAuthenticateDeviceEx function


## -description


The <b>BluetoothAuthenticateDeviceEx</b> function sends an authentication request to a remote Bluetooth device. Additionally, this function allows for out-of-band data to be passed into the function call for the device being authenticated.
<div class="alert"><b>Note</b>  This API is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters




### -param hwndParentIn [in, optional]

The window to parent the authentication wizard. If <b>NULL</b>, the 
wizard will be parented off the desktop.


### -param hRadioIn [in, optional]

A valid local radio handle or <b>NULL</b>. If <b>NULL</b>, then all radios will
          be tried. If any of the radios succeed, then the call will
succeed.


### -param pbtdiInout [in, out]

A pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure describing the device          being authenticated.


### -param pbtOobData [in, optional]

Pointer to device specific out-of-band data to be provided with this API call.  If <b>NULL</b>, then a UI is
          displayed to continue the authentication process.
If not <b>NULL</b>, no UI is displayed.

<div class="alert"><b>Note</b>  If a callback is registered using <a href="https://msdn.microsoft.com/c9838f27-3450-4d51-be58-ce515d06d5cb">BluetoothRegisterForAuthenticationEx</a>, then a UI will not be displayed.</div>
<div> </div>

### -param authenticationRequirement [in]

An <a href="https://msdn.microsoft.com/644372af-d613-4fd6-adcd-7faf0afb0033">BLUETOOTH_AUTHENTICATION_REQUIREMENTS</a>value that specifies the protection required for authentication.


## -returns



Returns ERROR_SUCCESS upon successful completion; returns the following error codes upon failure:

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
The user aborted the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The device structure specified in <i>pbdti</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The device in pbtdi is already been marked as authenticated.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure specified by <i>pbtdilInOut</i> must contain the address of a device to authenticate.  If the value of <i>pbtOobData</i> is not <b>NULL</b>, an attempt  will be made to authenticate the remote device with the provided out-of-band data.

For all other types of  authentication, the caller should register an authentication callback using <a href="https://msdn.microsoft.com/c9838f27-3450-4d51-be58-ce515d06d5cb">BluetoothRegisterForAuthenticationEx</a> and then respond to the relevant authentication method using <a href="https://msdn.microsoft.com/f23f90e3-c86f-44e4-a164-620105b19f08">BluetoothSendAuthenticationResponseEx</a>.


#### Examples

In the following example code a device has been found and an authentication request is  sent using <b>BluetoothAuthenticateDeviceEx</b>. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PBLUETOOTH_DEVICE_INFO pDeviceInfo; 
HRESULT status;
HANDLE hEvent = NULL;

HRESULT WINAPI AuthenticateService(){

	status = BluetoothAuthenticateDeviceEx( NULL,
					        NULL,
					        pDeviceInfo,
					        NULL,
					        MITMProtectionNotRequired );

	if ( ERROR_INVALID_PARAMETER == status ) {
		// goto Cleanup;
		// ...
		// Take cleanup action here,
		// ...
	}
//
// Wait for the Authentication callback to return before trying to unregister the handle
// Use an infinite timeout since the handle to the function that sets the event is being
// deleted
//

	if ( WAIT_FAILED == WaitForSingleObject(hEvent, INFINITE) ) {
        	status = GetLastError();
        	// goto Cleanup;
		// ...
		// Take cleanup action here,
		// ...
	}

      return status;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>
 

 

