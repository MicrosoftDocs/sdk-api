---
UID: NF:bluetoothapis.BluetoothUnregisterAuthentication
title: BluetoothUnregisterAuthentication function (bluetoothapis.h)
description: The BluetoothUnregisterAuthentication function removes registration for a callback routine that was previously registered with a call to the BluetoothRegisterForAuthentication function.
helpviewer_keywords: ["BluetoothUnregisterAuthentication","BluetoothUnregisterAuthentication function [Bluetooth]","bluetooth.bluetoothunregisterauthentication","bluetoothapis/BluetoothUnregisterAuthentication"]
old-location: bluetooth\bluetoothunregisterauthentication.htm
tech.root: bluetooth
ms.assetid: bfb1a18c-e5b1-4053-8652-5a76b196bebe
ms.date: 12/05/2018
ms.keywords: BluetoothUnregisterAuthentication, BluetoothUnregisterAuthentication function [Bluetooth], bluetooth.bluetoothunregisterauthentication, bluetoothapis/BluetoothUnregisterAuthentication
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
 - BluetoothUnregisterAuthentication
 - bluetoothapis/BluetoothUnregisterAuthentication
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
 - BluetoothUnregisterAuthentication
---

# BluetoothUnregisterAuthentication function


## -description

The <b>BluetoothUnregisterAuthentication</b> function removes registration for a callback routine that was previously registered with a call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a> function.

## -parameters

### -param hRegHandle

Handle returned by a previous call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a> function.

## -returns

Returns <b>TRUE</b> when the authentication registration is successfully removed. Returns <b>FALSE</b> if the specified handle is not successfully closed.

Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to obtain more information about the error. The following table  describes a common error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is <b>NULL</b>.

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



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>