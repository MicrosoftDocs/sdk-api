---
UID: NF:bluetoothapis.BluetoothSendAuthenticationResponse
title: BluetoothSendAuthenticationResponse function
author: windows-sdk-content
description: The BluetoothSendAuthenticationResponse function is called when an authentication request to send the passkey response is received.
old-location: bluetooth\bluetoothsendauthenticationresponse.htm
tech.root: Bluetooth
ms.assetid: 4483f04e-09a2-4bd4-879c-c3a263c685de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BluetoothSendAuthenticationResponse, BluetoothSendAuthenticationResponse function [Bluetooth], bluetooth.bluetoothsendauthenticationresponse, bluetoothapis/BluetoothSendAuthenticationResponse
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
api_name:
 - BluetoothSendAuthenticationResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothSendAuthenticationResponse function


## -description


The <b>BluetoothSendAuthenticationResponse</b> function is called when an authentication request
to send the passkey response is received.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/en-us/library/Cc766821(v=VS.85).aspx">BluetoothSendAuthenticationResponseEx</a> is recommended.</div><div> </div>

## -parameters




### -param hRadio

Optional handle to the local radio handle, or <b>NULL</b>. If <b>NULL</b>, the function attempts to send an authentication response on all local radios.


### -param pbtdi

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a> structure describing the Bluetooth device being authenticated. This can be the same structure passed to the callback function.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc766821(v=VS.85).aspx">BluetoothSendAuthenticationResponseEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

