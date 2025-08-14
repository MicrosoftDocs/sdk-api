---
UID: NF:bluetoothapis.BluetoothRegisterForAuthentication
title: BluetoothRegisterForAuthentication function (bluetoothapis.h)
description: The BluetoothRegisterForAuthentication function registers a callback function that is called when a particular Bluetooth device requests authentication.
helpviewer_keywords: ["BluetoothRegisterForAuthentication","BluetoothRegisterForAuthentication function [Bluetooth]","bluetooth.bluetoothregisterforauthentication","bluetoothapis/BluetoothRegisterForAuthentication"]
old-location: bluetooth\bluetoothregisterforauthentication.htm
tech.root: bluetooth
ms.assetid: f85dd076-9062-413f-863f-9d3baba322ad
ms.date: 12/05/2018
ms.keywords: BluetoothRegisterForAuthentication, BluetoothRegisterForAuthentication function [Bluetooth], bluetooth.bluetoothregisterforauthentication, bluetoothapis/BluetoothRegisterForAuthentication
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
 - BluetoothRegisterForAuthentication
 - bluetoothapis/BluetoothRegisterForAuthentication
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
 - BluetoothRegisterForAuthentication
---

# BluetoothRegisterForAuthentication function


## -description

The <b>BluetoothRegisterForAuthentication</b> function registers a callback function that is called when a particular Bluetooth device requests authentication.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthenticationex">BluetoothRegisterForAuthenticationEx</a> is recommended.</div><div> </div>

## -parameters

### -param pbtdi

Pointer to a  <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structure. The Address member is used for comparison.

### -param phRegHandle

Pointer to a structure in which the registration HANDLE is stored. Call the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a> to close the handle.

### -param pfnCallback

Function to be called when the authentication event occurs. The function should match the prototype described in PFN_AUTHENTICATION_CALLBACK.

### -param pvParam

Optional parameter to be passed through the callback function.

## -returns

Returns ERROR_SUCCESS upon successful completion, and a valid registration handle was returned in <i>phRegHandle</i>. Any other return value indicates failure.

Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to obtain more information about the error. The following table  describes a common error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>