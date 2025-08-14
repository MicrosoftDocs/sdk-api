---
UID: NF:bluetoothapis.BluetoothSendAuthenticationResponse
title: BluetoothSendAuthenticationResponse function (bluetoothapis.h)
description: The BluetoothSendAuthenticationResponse function is called when an authentication request to send the passkey response is received.
helpviewer_keywords: ["BluetoothSendAuthenticationResponse","BluetoothSendAuthenticationResponse function [Bluetooth]","bluetooth.bluetoothsendauthenticationresponse","bluetoothapis/BluetoothSendAuthenticationResponse"]
old-location: bluetooth\bluetoothsendauthenticationresponse.htm
tech.root: bluetooth
ms.assetid: 4483f04e-09a2-4bd4-879c-c3a263c685de
ms.date: 12/05/2018
ms.keywords: BluetoothSendAuthenticationResponse, BluetoothSendAuthenticationResponse function [Bluetooth], bluetooth.bluetoothsendauthenticationresponse, bluetoothapis/BluetoothSendAuthenticationResponse
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
 - BluetoothSendAuthenticationResponse
 - bluetoothapis/BluetoothSendAuthenticationResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-bluetooth-apis-l1-1-0.dll
 - bthprops.cpl
api_name:
 - BluetoothSendAuthenticationResponse
---

# BluetoothSendAuthenticationResponse function


## -description

The <b>BluetoothSendAuthenticationResponse</b> function is called when an authentication request
to send the passkey response is received.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponseex">BluetoothSendAuthenticationResponseEx</a> is recommended.</div><div> </div>

## -parameters

### -param hRadio

Optional handle to the local radio handle, or <b>NULL</b>. If <b>NULL</b>, the function attempts to send an authentication response on all local radios.

### -param pbtdi

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure describing the Bluetooth device being authenticated. This can be the same structure passed to the callback function.

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

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BluetoothAuthenticateMultipleDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">BluetoothEnableDiscovery</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenableincomingconnections">BluetoothEnableIncomingConnections</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisconnectable">BluetoothIsConnectable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponseex">BluetoothSendAuthenticationResponseEx</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>