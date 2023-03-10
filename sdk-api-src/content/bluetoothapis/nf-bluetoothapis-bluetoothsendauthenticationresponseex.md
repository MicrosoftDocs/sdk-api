---
UID: NF:bluetoothapis.BluetoothSendAuthenticationResponseEx
title: BluetoothSendAuthenticationResponseEx function (bluetoothapis.h)
description: The BluetoothSendAuthenticationResponseEx function is called when an authentication request to send the passkey or a Numeric Comparison response is made.
helpviewer_keywords: ["BluetoothSendAuthenticationResponseEx","BluetoothSendAuthenticationResponseEx function [Bluetooth]","bluetooth.bluetoothsendauthenticationresponseex","bluetoothapis/BluetoothSendAuthenticationResponseEx"]
old-location: bluetooth\bluetoothsendauthenticationresponseex.htm
tech.root: bluetooth
ms.assetid: f23f90e3-c86f-44e4-a164-620105b19f08
ms.date: 12/05/2018
ms.keywords: BluetoothSendAuthenticationResponseEx, BluetoothSendAuthenticationResponseEx function [Bluetooth], bluetooth.bluetoothsendauthenticationresponseex, bluetoothapis/BluetoothSendAuthenticationResponseEx
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
 - BluetoothSendAuthenticationResponseEx
 - bluetoothapis/BluetoothSendAuthenticationResponseEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothSendAuthenticationResponseEx
---

# BluetoothSendAuthenticationResponseEx function


## -description

The <b>BluetoothSendAuthenticationResponseEx</b> function is called when an authentication request
to send the passkey or a Numeric Comparison response is made.
<div class="alert"><b>Note</b>  This API is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters

### -param hRadioIn [in, optional]

A handle of the Bluetooth radio device to specify local service information for.

### -param pauthResponse [in]

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_authenticate_response">BLUETOOTH_AUTHENTICATE_RESPONSE</a> structure containing the response to the <b>BTH_REMOTE_AUTHENTICATE_REQUEST</b> event.

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
The device was denied the passkey response. This may also indicate a communications problem with the local radio device.

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

## -remarks

Callers can only use this function to respond to a pending authentication request.  Applications should register with <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthenticationEx</a> in order to be notified of incoming authentication requests.  

Only the <b>BLUETOOTH_AUTHENTICATION_METHOD_LEGACY</b>, <b>BLUETOOTH_AUTHENTICATION_METHOD_NUMERIC_COMPARISON</b> and <b>BLUETOOTH_AUTHENTICATION_METHOD_PASSKEY_NOTIFICATION</b> response types are valid.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>