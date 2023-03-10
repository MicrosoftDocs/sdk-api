---
UID: NF:bluetoothapis.BluetoothIsDiscoverable
title: BluetoothIsDiscoverable function (bluetoothapis.h)
description: The BluetoothIsDiscoverable function determines whether a Bluetooth radio or radios is discoverable.
helpviewer_keywords: ["BluetoothIsDiscoverable","BluetoothIsDiscoverable function [Bluetooth]","bluetooth.bluetoothisdiscoverable","bluetoothapis/BluetoothIsDiscoverable"]
old-location: bluetooth\bluetoothisdiscoverable.htm
tech.root: bluetooth
ms.assetid: 33d34e36-dc17-4029-91bd-53ece5a93b4b
ms.date: 12/05/2018
ms.keywords: BluetoothIsDiscoverable, BluetoothIsDiscoverable function [Bluetooth], bluetooth.bluetoothisdiscoverable, bluetoothapis/BluetoothIsDiscoverable
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
 - BluetoothIsDiscoverable
 - bluetoothapis/BluetoothIsDiscoverable
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
 - BluetoothIsDiscoverable
---

# BluetoothIsDiscoverable function


## -description

The <b>BluetoothIsDiscoverable</b> function determines whether a Bluetooth radio or radios is discoverable.

## -parameters

### -param hRadio

Valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, discovery is determined for all local radios; if any radio is discoverable, the function call succeeds.

## -returns

Returns <b>TRUE</b> if at least one Bluetooth radio is discoverable. Returns <b>FALSE</b> if no Bluetooth radios are discoverable.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BluetoothAuthenticateMultipleDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">BluetoothEnableDiscovery</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenableincomingconnections">BluetoothEnableIncomingConnections</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisconnectable">BluetoothIsConnectable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>