---
UID: NF:bluetoothapis.BluetoothIsConnectable
title: BluetoothIsConnectable function (bluetoothapis.h)
description: The BluetoothIsConnectable function determines whether a Bluetooth radio or radios is connectable.
helpviewer_keywords: ["BluetoothIsConnectable","BluetoothIsConnectable function [Bluetooth]","bluetooth.bluetoothisconnectable","bluetoothapis/BluetoothIsConnectable"]
old-location: bluetooth\bluetoothisconnectable.htm
tech.root: bluetooth
ms.assetid: e20ad938-cab4-4017-95bf-8d6843f048eb
ms.date: 12/05/2018
ms.keywords: BluetoothIsConnectable, BluetoothIsConnectable function [Bluetooth], bluetooth.bluetoothisconnectable, bluetoothapis/BluetoothIsConnectable
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
 - BluetoothIsConnectable
 - bluetoothapis/BluetoothIsConnectable
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
 - BluetoothIsConnectable
---

# BluetoothIsConnectable function


## -description

The <b>BluetoothIsConnectable</b> function determines whether a Bluetooth radio or radios is connectable.

## -parameters

### -param hRadio

Valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, all local radios are checked for connectability; if any radio is connectable, the function call succeeds.

## -returns

Returns <b>TRUE</b> if at least one Bluetooth radio is accepting incoming connections. Returns <b>FALSE</b> if no radios are accepting incoming connections.

## -remarks

If multiple Bluetooth radios exist, the first radio to return that it is connectable causes the <b>BluetoothIsConnectable</b> function to succeed.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BluetoothAuthenticateMultipleDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenablediscovery">BluetoothEnableDiscovery</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenableincomingconnections">BluetoothEnableIncomingConnections</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>