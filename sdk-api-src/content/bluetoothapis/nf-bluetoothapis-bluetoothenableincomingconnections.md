---
UID: NF:bluetoothapis.BluetoothEnableIncomingConnections
title: BluetoothEnableIncomingConnections function (bluetoothapis.h)
description: The BluetoothEnableIncomingConnections function modifies whether a local Bluetooth radio accepts incoming connections.
helpviewer_keywords: ["BluetoothEnableIncomingConnections","BluetoothEnableIncomingConnections function [Bluetooth]","bluetooth.bluetoothenableincomingconnections","bluetoothapis/BluetoothEnableIncomingConnections"]
old-location: bluetooth\bluetoothenableincomingconnections.htm
tech.root: bluetooth
ms.assetid: 8f9c133e-e647-45c8-b2c6-372b18345637
ms.date: 12/05/2018
ms.keywords: BluetoothEnableIncomingConnections, BluetoothEnableIncomingConnections function [Bluetooth], bluetooth.bluetoothenableincomingconnections, bluetoothapis/BluetoothEnableIncomingConnections
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
 - BluetoothEnableIncomingConnections
 - bluetoothapis/BluetoothEnableIncomingConnections
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
 - BluetoothEnableIncomingConnections
---

# BluetoothEnableIncomingConnections function


## -description

The <b>BluetoothEnableIncomingConnections</b> function modifies whether a local Bluetooth radio accepts incoming connections.

## -parameters

### -param hRadio

Valid local radio handle for which to change whether incoming connections are enabled, or <b>NULL</b>. If <b>NULL</b>, the attempt to modify incoming connection acceptance iterates through all local radios; if any radio is modified by the call, the function call succeeds.

### -param fEnabled

Flag specifying whether incoming connection acceptance is to be enabled or disabled. Set to <b>TRUE</b> to enable incoming connections, set to <b>FALSE</b> to disable incoming connections.

## -returns

Returns <b>TRUE</b> if the incoming connection  state was successfully changed. If <i>hRadio</i> is <b>NULL</b>, a return value of <b>TRUE</b> indicates that at least one local radio state was successfully changed. Returns <b>FALSE</b> if incoming connection  state was not changed; if <i>hRadio</i> was <b>NULL</b>, no radio accepted the state change.

## -remarks

 A  radio that is non-connectable is non-discoverable. The radio must be made non-discoverable  prior to making a radio non-connectable. Failure to make a radio non-discoverable prior to making it non-connectable will result in failure of the <b>BluetoothEnableIncomingConnections</b> function call.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BluetoothAuthenticateMultipleDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">BluetoothEnableDiscovery</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisconnectable">BluetoothIsConnectable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>