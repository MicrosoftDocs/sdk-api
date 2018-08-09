---
UID: NF:bluetoothapis.BluetoothSendAuthenticationResponse
title: BluetoothSendAuthenticationResponse function
author: windows-sdk-content
description: The BluetoothSendAuthenticationResponse function is called when an authentication request to send the passkey response is received.
old-location: bluetooth\bluetoothsendauthenticationresponse.htm
old-project: bluetooth
ms.assetid: 4483f04e-09a2-4bd4-879c-c3a263c685de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BluetoothSendAuthenticationResponse, BluetoothSendAuthenticationResponse function [Bluetooth], bluetooth.bluetoothsendauthenticationresponse, bluetoothapis/BluetoothSendAuthenticationResponse
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
api_name:
 - BluetoothSendAuthenticationResponse
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothSendAuthenticationResponse function


## -description


The <b>BluetoothSendAuthenticationResponse</b> function is called when an authentication request
to send the passkey response is received.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/f23f90e3-c86f-44e4-a164-620105b19f08">BluetoothSendAuthenticationResponseEx</a> is recommended.</div><div> </div>

## -parameters




### -param hRadio

Optional handle to the local radio handle, or <b>NULL</b>. If <b>NULL</b>, the function attempts to send an authentication response on all local radios.


### -param pbtdi

Pointer to a <a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structure describing the Bluetooth device being authenticated. This can be the same structure passed to the callback function.


### -param pszPasskey

Pointer to a UNICODE zero-terminated string of the passkey response
to be sent back to the authenticating device. the <i>pszPasskey</i> parameter can be no larger than BLUETOOTH_MAX_PASSKEY_SIZE, excluding <b>NULL</b>. If translation to ANSI is performed, the <i>pszPasskey</i> parameter cannot be larger than 16 bytes, excluding <b>NULL</b>.


## -returns



 Returns ERROR_SUCCESS when the device accepts the passkey response; the device is authenticated. Any other return value indicates failure. The following table  describes common errors:

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
The Bluetooth device denied the passkey response. This error is also returned if a communication problem exists with the local radio.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The device returned a failure code during authentication.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/8f9c133e-e647-45c8-b2c6-372b18345637">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/e20ad938-cab4-4017-95bf-8d6843f048eb">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/f23f90e3-c86f-44e4-a164-620105b19f08">BluetoothSendAuthenticationResponseEx</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

